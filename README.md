Laptop
======

Laptop is a script to set up an OS X laptop for Rally project development.

Requirements
------------

We support:

* [OS X Mavericks (10.9)](https://itunes.apple.com/us/app/os-x-mavericks/id675248567)
* [OS X Yosemite (10.10)](https://www.apple.com/osx/)

Older versions may work but aren't regularly tested. Bug reports for older
versions are welcome.

Install
-------

Read, then run the script:

    bash <(curl -s https://raw.githubusercontent.com/rallygroup/laptop/master/mac) 2>&1 | tee ~/laptop.log

Debugging
---------

Your last Laptop run will be saved to `~/laptop.log`. Read through it to see if
you can debug the issue yourself. If not, copy the lines where the script
failed into a [new GitHub
Issue](https://github.com/thoughtbot/laptop/issues/new) for us. Or, attach the
whole log file as an attachment.

What it sets up
---------------

* [Docker] for managing local environments
* [Exuberant Ctags] for indexing files for vim tab completion
* [Heroku Toolbelt] for interacting with the Heroku API
* [Homebrew] for managing operating system libraries
* [ImageMagick] for cropping and resizing images
* [Node.js] and [NPM], for running apps and installing JavaScript packages
* [NVM] for managing versions of Node.js
* [MySQL] for storing relational data
* [Qt] for headless JavaScript testing via Capybara Webkit
* [Rails] gem for writing web applications
* [Rbenv] for managing versions of Ruby
* [Redis] for storing key-value data
* [The Silver Searcher] for finding things in files
* [wget] for downloading remote files
* [Zsh] as your shell

[Docker]: http://www.docker.com/
[Exuberant Ctags]: http://ctags.sourceforge.net/
[gh]: https://github.com/jingweno/gh
[Heroku Toolbelt]: https://toolbelt.heroku.com/
[Homebrew]: http://brew.sh/
[ImageMagick]: http://www.imagemagick.org/
[Node.js]: http://nodejs.org/
[NPM]: https://www.npmjs.org/
[NVM]: https://github.com/creationix/nvm
[MySQL]: http://www.mysql.org/
[Qt]: http://qt-project.org/
[Rails]: http://rubyonrails.org/
[Rbenv]: https://github.com/sstephenson/rbenv
[Redis]: http://redis.io/
[Ruby Build]: https://github.com/sstephenson/ruby-build
[Ruby]: https://www.ruby-lang.org/en/
[The Silver Searcher]: https://github.com/ggreer/the_silver_searcher
[wget]: https://www.gnu.org/software/wget
[Zsh]: http://www.zsh.org/

It should take less than 15 minutes to install (depends on your machine).

Laptop can be run multiple times on the same machine safely. It will upgrade
already installed packages and install and activate a new version of ruby (if
one is available).

Make your own customizations
----------------------------

Put your customizations in `~/.laptop.local`. For example, your
`~/.laptop.local` might look like this:

    #!/bin/sh

    brew tap caskroom/cask
    brew install brew-cask

    brew cask install dropbox
    brew cask install google-chrome
    brew cask install rdio

You should write your customizations such that they can be run safely more than
once. See the `mac` script for examples.

Credits
-------

![thoughtbot](http://thoughtbot.com/assets/tm/logo.png)

Laptop is maintained and funded by [thoughtbot, inc](http://thoughtbot.com/community).
The names and logos for thoughtbot are trademarks of thoughtbot, inc.

Thank you, [contributors](https://github.com/thoughtbot/laptop/graphs/contributors)!

Contributing
------------

Edit the `mac` file.

License
-------

Laptop is © 2011-2014 thoughtbot, inc. It is free software, and may be
redistributed under the terms specified in the LICENSE file.
