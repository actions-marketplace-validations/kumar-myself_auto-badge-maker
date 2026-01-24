# auto-badge-maker
🤖 Creates beautiful badges for your GitHub README automatically!


steps:
  - uses: actions/checkout@v4
  
  - name: Create badge
    id: badge
    uses: kumar-myself/auto-badge-maker@v1
    with:
      text: 'Stars-100'
      color: 'brightgreen'
  
  - name: Use the badge
    run: |
      echo "${{ steps.badge.outputs.badge-markdown }}" >> README.md
  
  - name: Commit
    uses: stefanzweifel/git-auto-commit-action@v5
