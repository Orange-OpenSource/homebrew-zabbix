# homebrew-zabbix

This is a 3rd party tap for [Homebrew](http://brew.sh/). It provides formula for `zabbix` which includes options for enabling additional features and libraries.

Contents:

- [Installation and usage](#installation-and-usage)
- [Updating](#updating)
- [FAQ](#faq)
- [Issues](#issues)
- [Maintainers](#maintainers)

## Installation and usage

In order to use this tap, you need to install Homebrew or Linuxbrew.

To use, first tap and pin this repo:

```
brew tap phoenixadb/zabbix
brew tap-pin phoenixadb/zabbix
```

**Note:** If you already have `zabbix` installed from Homebrew core, you need to first run `brew uninstall zabbix` before you can use this tap.

### Default installation

To install the default version of the formula, run:

```
brew install zabbix
```

### Installing with options

To see the list of supported options for this formula, run:

```
brew options zabbix
```

Then, you can run:

```
brew install zabbix --with-<option1> --with-<option2> ...
```

### Installing latest Git version (`HEAD`)

FFmpeg recommends installing the latest Git master version over a release. This formula builds the latest release by default, but you can install the latest Git version by adding the `--HEAD` option:

```
brew install zabbix --HEAD
```

### Installing *everything*

To compile and install zabbix with *all* options, just run:

```
brew install zabbix $(brew options zabbix --compact)
```

Note that this will perform a full build of ffmpeg and its dependencies, which may take a while depending on your machine's capabilities.

## Updating

To update Homebrew and upgrade the formula to the most recent stable release:

```
brew update && brew upgrade zabbix
```

Or, if you are using the `HEAD` version and want to update to the latest commit:

```
brew update && brew upgrade ffmpeg --fetch-HEAD
```

## FAQ

### What is `tap-pin`?

Using `brew tap-pin` gives this tap's `zabbix` formula priority over homebrew-core to make installation simpler. Now `zabbix` will refer to this tap's formula.

If you don't want to pin this tap, you can still reference this tap's ffmpeg formula directly with `phoenixadb/zabbix/zabbix`. Tap pinning will not influence an `zabbix` dependency in another formula.

To unpin the tap, simply run `brew tap-unpin phoenixadb/zabbix`.

### I used the old repository name, what should I do?

This repo was previously named `zabbix-with-options`. While there is a redirect to the new repository name, you should update to the tap's new name. To do so, run:

```
brew untap phoenixadb/zabbix-with-options
brew tap phoenixadb/zabbix
brew tap-pin phoenixadb/zabbix
```

## Issues

To report issues, please [file an issue on GitHub](https://github.com/varenc/homebrew-zabbix/issues). Please note that we will only be able to help with issues that are exclusive to this tap.

If the problem is reproducible with the `homebrew-core` version of `zabbix`, please file it [on their tracker](https://github.com/Homebrew/homebrew-core/).

## Maintainers

- Arnaud de Bock (`@phoenixadb`)


