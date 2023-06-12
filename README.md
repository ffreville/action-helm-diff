# action-helm-diff
A GitHub action to use the helm diff plugin (https://github.com/databus23/helm-diff)

## Example

```

name: CI
on:
  pull_request:
    branches: [ main ]
jobs:
  scan:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - name: Helm diff
        uses: ffreville/action-helm-diff@main
        with:
          release_name: "my-project"
          chart_directory: "chart"

```


