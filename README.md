# Straddle Homebrew tap

Install and update the [Straddle CLI](https://github.com/straddle-build/straddle-cli) on macOS with Homebrew. The `straddle` command provides terminal and agent access to Straddle's Pay by Bank and Embed APIs, plus local payment analysis.

## Install

With [Homebrew](https://brew.sh) installed, add the CLI and check its version:

```sh
brew install straddle-build/tap/straddle
straddle --version
```

The version command prints `straddle` followed by the installed version. The cask selects the binary for your Mac's Apple silicon or Intel processor.

## Update

Refresh Homebrew's package definitions, then upgrade the CLI:

```sh
brew update
brew upgrade --cask straddle-build/tap/straddle
straddle --version
```

## Start using the CLI

Inspect the available commands:

```sh
straddle --help
```

Follow the CLI's [authentication and sandbox setup](https://github.com/straddle-build/straddle-cli#authentication) to make your first API request. For npm, Linux, Windows, or source builds, see [other installation methods](https://github.com/straddle-build/straddle-cli#install).

## Maintain the tap

The CLI's GoReleaser workflow generates [`Casks/straddle.rb`](Casks/straddle.rb) from a published release, pushes it to a `straddle-<version>` branch, and opens a pull request. A maintainer reviews the change and merges it after the tap checks pass. The cask uses release archives and their SHA-256 checksums.

Make release configuration changes in the [CLI repository](https://github.com/straddle-build/straddle-cli). See its [release process](https://github.com/straddle-build/straddle-cli/blob/main/OPERATIONS.md#release) for cask generation and publication details.

Report Homebrew installation problems in [this repository's issues](https://github.com/straddle-build/homebrew-tap/issues) and CLI behavior problems in the [CLI issue tracker](https://github.com/straddle-build/straddle-cli/issues).
