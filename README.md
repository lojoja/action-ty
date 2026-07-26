# action-ty

A composite action that type checks with [ty](https://docs.astral.sh/ty/).

This repository is not meant to be referenced in third-party workflows; please fork the repository if you would like to use it in your project.

## Inputs

| Name              | Description                                       | Required | Default |
| ----------------- | ------------------------------------------------- | :------: | ------- |
| cache             | Whether to cache project dependencies.            |          | "true"  |
| package_manager   | The package manager to use ("poetry" or "uv").    |          | "uv"    |
| python_version    | The python version to use in SemVer range syntax. |          | "3.14"  |
| working_directory | The working directory for the action.             |          | "."     |

## Examples

### ty Check

```
jobs:
  ty:
    runs-on: ubuntu-latest
    steps:
      - uses: lojoja/action-ty@main
        with:
          cache: "true"
          package_manager: uv
          python_version: "3.14"
```

## License

action-ty is released under the [MIT License](./LICENSE)
