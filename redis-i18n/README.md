# Redis stores for I18n

__`redis-i18n`__ provides a Redis backend for __I18n__. It natively supports object marshalling, timeouts, single or multiple nodes and namespaces.

## Redis Installation

### Option 1: Homebrew

MacOS X users should use [Homebrew](https://github.com/mxcl/homebrew) to install Redis:

    brew install redis

### Option 2: From Source

Download and install Redis from [http://redis.io](http://redis.io/)

	wget http://redis.googlecode.com/files/redis-2.4.5.tar.gz
    tar -zxf redis-2.4.5.tar.gz
    mv redis-2.4.5 redis
    cd redis
    make

## Usage

    # Gemfile
	gem 'redis-i18n'

### Backend:

	I18n.backend = I18n::Backend::Redis.new

#### Configuration

For advanced configuration options, please check the [Redis Store Wiki](https://github.com/jodosha/redis-store/wiki).

## Running tests

    git clone git://github.com/jodosha/redis-store.git
	cd redis-store/redis-i18n
	gem install bundler --pre # required version: 1.1.rc
	bundle exec rake

If you are on **Snow Leopard** you have to run `env ARCHFLAGS="-arch x86_64" bundle exec rake`

## Copyright

(c) 2009 - 2011 Luca Guidi - [http://lucaguidi.com](http://lucaguidi.com), released under the MIT license
