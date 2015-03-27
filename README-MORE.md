# irbtools-more

`irbtools-more` adds more IRB gems which may not build out-of-the-box.
Currently included: `bond` for better auto-completion and `looksee` for great
method introspection. The `did_you_mean` gem is included to improve error
stacktraces. It also adds the `binding_of_caller` gem to enable starting IRB
by just calling `repl` anywhere in your code. See the [irbtools
readme](https://github.com/janlelis/irbtools) for details.

## Setup

### With bundler

In your `Gemfile` put:

    gem 'irbtools-more', require: 'debugging/repl'

### With bundler (debundle hack)

See [debundle.rb](https://github.com/janlelis/debundle.rb).

### Without bundler

    gem install irbtools-more

## Usage

To use it, put the following in your `~/.irbrc` file (this file is loaded
every time you start an irb, just create the file, if it does not exist, yet):

    require 'irbtools/more'

If you want to customize which libraries you want to use, you can load
irbtools-more explicitely:

    require 'irbtools/configure'
    Irbtools.add_package :more # adds this extension package
    Irbtools.start

## J-_-L

Copyright (c) 2010-2015 Jan Lelis, http://janlelis.com. See MIT-LICENSE for
details.
