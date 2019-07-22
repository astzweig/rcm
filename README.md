rcm
===

This is a management suite for dotfiles. **See [the tutorial][rcm7] to get
started quickly.**

It assumes that you have a separate dotfiles directory, or are
interested in creating one.

The programs provided are [rcup(1)][rcup1], [mkrc(1)][mkrc1], [rcdn(1)][rcdn1],
and [lsrc(1)][lsrc1]. They are explained in [the tutorial][rcm7] and configured
using [rcrc(5)][rcrc5].

Installation
------------

Alpine Linux:

    sudo apk add rcm

Arch Linux:

  https://aur.archlinux.org/packages/rcm/

Debian-based:

    wget -qO - https://apt.thoughtbot.com/thoughtbot.gpg.key | sudo apt-key add -
    echo "deb https://apt.thoughtbot.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/thoughtbot.list
    sudo apt-get update
    sudo apt-get install rcm

Fedora:

    sudo dnf install rcm

FreeBSD:

    sudo pkg install rcm

Gentoo:

    emerge app-admin/rcm

Korora:

  64-bit Korora 23:

    sudo dnf copr enable seeitcoming/rcm fedora-23-x86_64
    sudo dnf install rcm

  Korora is similar to Fedora but with [an additional version and architecture
  specification][copr-fedora-korora]. Replace `fedora-23-x86_64` as
  appropriate.

  [copr-fedora-korora]: https://kororaproject.org/about/news/when-adding-a-copr-repo-to-korora-fails

macOS with Homebrew:

    brew tap thoughtbot/formulae
    brew install rcm

macOS with MacPorts:

    port install rcm

OpenBSD:

    doas pkg_add rcm

openSUSE/RHEL/CentOS: [instructions](http://software.opensuse.org/download.html?project=utilities&package=rcm)

Ubuntu (19.04 or later):

    sudo apt update
    sudo apt install rcm

Ubuntu (12.04, 14.04, 16.04, 18.04, or 18.10):

    sudo apt-get install software-properties-common
    sudo add-apt-repository ppa:martin-frost/thoughtbot-rcm
    sudo apt-get update
    sudo apt-get install rcm

Void Linux:

    sudo xbps-install -S rcm

Elsewhere:

This uses the standard GNU autotools, so it's the normal dance:

    curl -LO https://thoughtbot.github.io/rcm/dist/rcm-1.3.3.tar.gz &&

    sha=$(sha256 rcm-1.3.3.tar.gz | cut -f1 -d' ') &&
    [ "$sha" = "935524456f2291afa36ef815e68f1ab4a37a4ed6f0f144b7de7fb270733e13af" ] &&

    tar -xvf rcm-1.3.3.tar.gz &&
    cd rcm-1.3.3 &&

    ./configure &&
    make &&
    sudo make install

For more, see `INSTALL`.

Programs
--------

* [rcup(1)][rcup1] is the main program. It is used to install and update
  dotfiles, with support for tags, host-specific files, and multiple source
  directories.
* [rcdn(1)][rcdn1] is the opposite of [rcup(1)][rcup1].
* [mkrc(1)][mkrc1] is for introducing a dotfile into your dotfiles directory,
  with support for tags and multiple source directories.
* [lsrc(1)][lsrc1] shows you all your dotfiles and where they would be
  symlinked to. It is used by [rcup(1)][rcup1] but is provided for your own
  use, too.

[rcup1]: http://thoughtbot.github.io/rcm/rcup.1.html
[mkrc1]: http://thoughtbot.github.io/rcm/mkrc.1.html
[rcdn1]: http://thoughtbot.github.io/rcm/rcdn.1.html
[lsrc1]: http://thoughtbot.github.io/rcm/lsrc.1.html
[rcm7]: http://thoughtbot.github.io/rcm/rcm.7.html
[rcrc5]: http://thoughtbot.github.io/rcm/rcrc.5.html

Support
-------

Pull requests welcome; see `CONTRIBUTING.md`.

License
-------

Copyright 2013 Mike Burns. BSD license.
Copyright 2014-2015 thoughtbot. BSD license.

## About thoughtbot

![thoughtbot](http://presskit.thoughtbot.com/images/thoughtbot-logo-for-readmes.svg)

RCM is maintained and funded by thoughtbot, inc.
The names and logos for thoughtbot are trademarks of thoughtbot, inc.

We adore open source software.
See [our other projects][community].
We are [available for hire][hire].

[community]: https://thoughtbot.com/community?utm_source=github
[hire]: https://thoughtbot.com/hire-us?utm_source=github
