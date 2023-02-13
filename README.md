# Welcome to your organization's demo respository
This code repository (or "repo") is designed to demonstrate the best GitHub has to offer with the least amount of noise.

The repo includes an `index.html` file (so it can render a web page), two GitHub Actions workflows, and a CSS stylesheet dependency.
name: Auto Assign
on:
  issues:
    types: [opened]
  pull_request:
    types: [opened]
jobs:
  run:
    runs-on: ubuntu-latest
    steps:
      - uses: wow-actions/auto-assign@v1
        with:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
          CONFIG_FILE: .github/auto-assign.yml
