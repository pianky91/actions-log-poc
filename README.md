# actions-log-poc
name: Actions Log Injection PoC

on:
  pull_request:

jobs:
  log-test:
    runs-on: ubuntu-latest
    steps:
      - name: Print PR data
        run: |
          echo "PR Title: ${{ github.event.pull_request.title }}"
          echo "PR Body: ${{ github.event.pull_request.body }}"
          echo "PR Branch: ${{ github.event.pull_request.head.ref }}"
          echo "Actor: ${{ github.actor }}"
