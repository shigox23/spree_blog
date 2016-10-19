SpreeBlog
===========

Introduction goes here.

Installation
------------

Add spree_blog to your Gemfile:

```ruby
gem 'spree_blog', github: 'shigox23/spree_blog', branch: '3-1-stable'
```
The branch option is important: it currently only supports Spree 3.1


Bundle your dependencies and run the installation generator:

```shell
bundle
bundle exec rails g spree_blogit:install
```


You don't need to run this again if you've already done so
```shell
bundle exec rake acts_as_taggable_on_engine:install:migrations
```

This will run any pending migrations
```shell
bundle exec rake db:migrate
```

Testing
-------

First bundle your dependencies, then run `rake`. `rake` will default to building the dummy app if it does not exist, then it will run specs. The dummy app can be regenerated by using `rake test_app`.

```shell
bundle
bundle exec rake
```

When testing your applications integration with this extension you may use it's factories.
Simply add this require statement to your spec_helper:

```ruby
require 'spree_blogit/factories'
```

Copyright (c) 2016 [name of extension creator], released under the New BSD License
