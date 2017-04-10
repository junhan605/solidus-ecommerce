# README

This application is a e-commerce site base on Solidus framework built in Ruby on Rails.
Solidus is a complete open source e-commerce solution built with Ruby on Rails. It is a fork of Spree.

* Ruby version

  Ruby 2.4
  Rails 5.0.2

* System dependencies

  ImageMagick

* Configuration

  See https://github.com/solidusio/solidus
  Note: For building on rails 5.0.2, run "bundle update" command after run "bundle install" command.

* To create a new Rails app, run below commands:
  > rvm use ruby-2.4
  > rvm gemset create rails-5.0.2
  > rvm gemset use rails-5.0.2
  > gem install bundler
  > gem install rails '5.0.2'
  > rails new solidus-ecommerce
  > cd solidus-ecommerce

* To add solidus, begin with a Rails 5 application. Add the following to your Gemfile.

  gem 'solidus'
  gem 'solidus_auth_devise'

* Run bundle commands
  > bundle install
  > bundle update

* After installing gems, you'll have to run the generators to create necessary configuration files and migrations.
  > bundle exec rails g spree:install
  > bundle exec rails g solidus:auth:install
  > bundle exec rake railties:install:migrations

* Run migrations to create the new models in the database.
  > bundle exec rake db:migrate
  > bundle exec rake railties:install:migrations
  > bundle exec rake db:migrate
  > bundle exec rake db:seed
  > bundle exec rake spree_sample:load

* Run a E-commerce server
  > bundle exec rails s

* Run in productions mode

  > bundle exec rake db:create RAILS_ENV=production

  > bundle exec rake db:migrate RAILS_ENV=production

  > bundle exec rake railties:install:migrations RAILS_ENV=production

  > bundle exec rake db:migrate RAILS_ENV=production

  > bundle exec rake db:seed RAILS_ENV=production

  > bundle exec rake spree_sample:load RAILS_ENV=production

  > bundle exec rake assets:precompile RAILS_ENV=production

  > bundle exec rails s -e production

* Performance

  You may notice that your Solidus store runs slowly in development mode. This can be because in development each css and javascript is loaded as a separate include. This can be disabled by adding the following to config/environments/development.rb.

  config.assets.debug = false

* Deployment instructions
