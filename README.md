# NO LONGER MAINTAINED

Use [pnpm/action-setup](https://github.com/pnpm/action-setup) instead.

# Setup PNPM

Install PNPM package manager.

## Inputs

### `version`

**Required** Version of PNPM to install.

### `dest`

**Optional** Where to store PNPM files.

### `bin_dest`

**Optional** Where to store executables (`pnpm` and `pnpx` commands).

### `registry`

**Optional** Registry to download PNPM from.

## Outputs

### `dest`

Expanded path of inputs#dest.

### `bin_dest`

Expanded path of inputs@bin_dest.

## Usage example

```yaml
on:
  - push
  - pull_request

jobs:
  runs-on: ubuntu-latest

  steps:
    - uses: actions/checkout@v2

    - uses: KSXGitHub/github-actions-setup-pnpm@master
      with:
        version: 4.11.1

    - name: Install dependencies
      run: pnpm install
```

## Notes

This action does not setup Node.js for you, use [actions/setup-node](https://github.com/actions/setup-node) yourself.

## License

[MIT](https://git.io/JfclH) © [Hoàng Văn Khải](https://github.com/KSXGitHub/)
