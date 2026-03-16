# mode

Create a modeful context within which to run sub-commands.

`mode` wraps any command that accepts sub-commands as arguments, giving you a persistent session where input is automatically prefixed with the command context and passed to the shell.

```
$ mode git
git> status
git> log --oneline
git> stash pop
git> exit
```

## Requirements

Ruby 2.7+

## Installation

Copy `mode` to somewhere on your PATH:

```
cp mode ~/bin/
chmod +x ~/bin/mode
```

## Usage

```
mode <command>
```

## Features

1. Provides line editing and history via Reline.
2. Exiting with `exit`, `quit`, or Ctrl-D or with an abbreviation thereof, such as: `e`, `ex`, `q`, `qu`, etc.

## Why?

On its own, `mode` is a mild convenience — fewer keystrokes when you're running a series of sub-commands against the same tool.

However, when combined with [shellac](https://github.com/thoran/shellac), which wraps shell commands into launchable macOS `.app` bundles for launching iTerm windows, it gives you a dedicated, findable workspace — launchable from Spotlight, the Dock, or a launcher such as Alfred, Hammerspoon, or Quicksilver.

## Examples

```
$ mode brew
brew> list
brew> update
brew> upgrade
```

```
$ mode gem
gem> list
gem> search reline
gem> install reline
```

```
$ mode docker
docker> ps -a
docker> images
docker> logs web
```

```
$ mode kubectl
kubectl> get pods
kubectl> describe pod web
kubectl> logs web
```

## See also

- [shellac](https://github.com/thoran/shellac) — Create macOS `.app` launchers for iTerm windows.
