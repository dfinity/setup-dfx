# dfinity/setup-dfx

The `dfinity/setup-dfx` repository provides a GitHub Action to streamline the installation of the `dfx` software development kit (SDK) for [Internet Computer](https://internetcomputer.org). This action simplifies the setup of Dfinity development environments in GitHub workflows.

## Usage

To use this action in your GitHub workflow, include it as a step in your workflow configuration:

```yml
jobs:
  example-job:
    runs-on: ubuntu-latest # macOS works too
    steps:
    - name: Checkout repository
      uses: actions/checkout@v2
    - name: Install dfx
      uses: dfinity/setup-dfx@main
    - name: Confirm successful installation
      run: dfx --version
```

The action is designed to run on both `ubuntu-latest` and `macOS` runners.

## Specifying a dfx Version

You can specify a particular version of dfx to install using the `dfx-version` input:

```yml
    - name: Install dfx
      uses: dfinity/setup-dfx@main
      with: 
        dfx-version: "0.14.2-beta.2"
```

## Inputs

| Input         | Description   |
|---------------|---------------|
| `dfx-version` | (Optional) The version of dfx to install. If not specified, the latest version will be installed.

## Contributing

Contributions to the `dfinity/setup-dfx` repository are welcome! 

## License

This project is licensed under the [Apache 2.0 License](LICENSE).

