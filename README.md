# Xcode::Install

[![Build Status](http://img.shields.io/travis/neonichu/xcode-install/master.svg?style=flat)](https://travis-ci.org/neonichu/xcode-install)
[![Coverage Status](https://coveralls.io/repos/neonichu/xcode-install/badge.svg)](https://coveralls.io/r/neonichu/xcode-install)
[![Gem Version](http://img.shields.io/gem/v/xcode-install.svg?style=flat)](http://badge.fury.io/rb/xcode-install)
[![Code Climate](http://img.shields.io/codeclimate/github/neonichu/xcode-install.svg?style=flat)](https://codeclimate.com/github/neonichu/xcode-install)

Install and update your Xcodes automatically.

```bash
$ gem install xcode-install
$ xcode-install install 6.3
```

## Installation

```bash
$ gem install xcode-install
```

## Usage

XcodeInstall will ask for your credentials to access the Apple Developer Center, they are stored
using the [CredentialsManager][1] of [Fastlane][2].

To list available versions:

```bash
$ xcode-install list
6.0.1
6.1
6.1.1
6.2
6.3
```

By default, only the latest major version is listed.

To install a certain version, simply:

```bash
$ xcode-install install 6.3
###########################################################               82.1%
######################################################################## 100.0%
Please authenticate for Xcode installation...

Xcode 6.3
Build version 6D570
```

This will download and install that version of Xcode. It will also be automatically selected.

## Limitations

This is a first shot, there are currently some limitations:

- No cleanup of caches in `~/Library/Caches/XcodeInstall` [#6](/../../issues/6)
- No automatic uninstallation [#3](/../../issues/3)
- No notion of installed versions [#1](/../../issues/1)
- No support for preleases [#5](/../../issues/5)

I will be addressing those in the future, but feel free to send PRs or report additional
bugs and shortcomings.

## Thanks

[This][3] downloading script which has been used for some inspiration, also [this][4]
for doing the installation.

## Contributing

1. Fork it ( https://github.com/[my-github-username]/xcode-install/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request


[1]: https://github.com/KrauseFx/CredentialsManager
[2]: http://fastlane.tools
[3]: http://atastypixel.com/blog/resuming-adc-downloads-cos-safari-sucks/
[4]: https://github.com/magneticbear/Jenkins_Bootstrap
