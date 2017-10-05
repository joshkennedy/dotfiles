# dotfiles

These are my dotfiles. Take anything you want, but at your own risk.

## What's Inside

* Core
  * Bash + [coreutils](https://en.wikipedia.org/wiki/GNU_Core_Utilities) + bash-completion
  * [Homebrew](https://brew.sh) + [homebrew-cask](https://caskroom.github.io)
  * Node.js + npm
  * GNU [sed](https://www.gnu.org/software/sed/), [grep](https://www.gnu.org/software/grep/), [Wget](https://www.gnu.org/software/wget/)
  * Git + [SourceTree](https://www.sourcetreeapp.com) + [hub](https://hub.github.com)
  * [rvm](https://rvm.io) (Ruby 2.1), [lunchy](https://github.com/eddiezane/lunchy)
  * Python 2
* Development (Node/JS/JSON)
  * [nodemon](https://nodemon.io),
* Graphics
  * [ffmpeg](https://www.ffmpeg.org)
  * [gifsicle](https://www.lcdf.org/gifsicle)
  * [imagemagick](https://www.imagemagick.org)
  * [svgo](https://github.com/svg/svgo)
* macOS Utilities
  * [Mackup](https://github.com/lra/mackup)
  * [Quick Look plugins](https://github.com/sindresorhus/quick-look-plugins)
* macOS Apps
  *

## Install

On a fresh installation of macOS:

    sudo softwareupdate -i -a
    xcode-select --install

Install the dotfiles with either Git or curl:

### Clone with Git

    git clone https://github.com/joshkennedy/dotfiles.git ~/.dotfiles
    source ~/.dotfiles/install.sh

### Remotely install using curl

Alternatively, you can install this into `~/.dotfiles` remotely without Git using curl:

    bash -c "`curl -fsSL https://raw.github.com/joshkennedy/dotfiles/master/remote-install.sh`"

Or, using wget:

    bash -c "`wget -O - --no-check-certificate https://raw.githubusercontent.com/joshkennedy/dotfiles/master/remote-install.sh`"

## The `dotfiles` command

    $ dotfiles help
    Usage: dotfiles <command>

    Commands:
       clean            Clean up caches (brew, npm, gem, rvm)
       edit             Open dotfiles in IDE (ws) and Git GUI (stree)
       help             This help message
       macos            Apply macOS system defaults
       test             Run tests
       update           Update packages and pkg managers (OS, brew, npm, gem)

## Customize/extend

You can put your custom settings, such as Git credentials in the `system/.custom` file which will be sourced from `.bash_profile` automatically. This file is in `.gitignore`.

Alternatively, you can have an additional, personal dotfiles repo at `~/.extra`.

* The runcom `.bash_profile` sources all `~/.extra/runcom/*.sh` files.
* The installer (`install.sh`) will run `~/.extra/install.sh`.

## Credits

- Huge thanks to @webpro for his [dotfiles](https://github.com/webpro/dotfiles) repo
