# Bobby's take on forkmantis's take on Greg's take on Holman's dotfiles

## Quickstart

Run this:

```sh
cd ~
git clone https://github.com/bobby-richard/dotfiles.git ~/dotfiles
cd ~/dotfiles
chmod +x **/*.sh
./redot
```

The `redot` script will walk you through everything and won't make any change to your computer without asking permission first.

## Conventions

### Global Conventions

- `bin/`: This directory is added to $PATH and is where to put useful scripts
- `homebrew/Brewfile`: This is a [Homebrew bundle file]("https://coderwall.com/p/afmnbq/homebrew-s-new-feature-brewfiles") that gets executed if you elect to do so when you run `redot`
- `lib` is where all the resources necessary for the redot command live.
- `osx/set-default`: This where you should set osx preferences

### Topic Conventions
- `<topic>/path.sh`: Any file with this name will be sourced during `$PATH` setup
- `<topic>/install.sh`: Any file with this name will be executed if you elect to do so when you run `redot`
- `<topic>/*.symlink`: Any file with the `.symlink` extension will be symlinked into your `$HOME` directory
- `<topic>/*.source`: Any file with the `.source` extension will be sourced when you run `redot`

### Sensitive Files

For files that should not be checked into source control, add .hide to the name i.e creds.hide.symlink
TODO: symlink these to dropbox/google drive


## I want my own dotfiles, what do I do?

If you like what you see here and what to get started, feel free to fork or clone the repo.  To make things easy, Ie have created a `barebones` branch which has all of my own modules stripped out, and contains only the redot script and other minimal stuff you need to get going.  

If you start with my master branch, you'll probably want to clean out a lot of my stuff and add your own.  If you start with the barebones branch, you should only need to make additive changes.
