# CapistranoLogs

Capistrano tasks that make it super easy to work with server logs.

## Installation

Add this line to your application's Gemfile:

    gem 'capistrano-logs', :require => false

Add this lone to your application's Capistrano configuration

    require 'capistrano-logs'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install capistrano-logs

## Usage

### logs:tail

You can now easily tail multiple servers at once by running:

    $ cap logs:tail

You can pass aditional commands to the `tail` command that gets run on the server. So:

    $ cap logs:tail -s logcommand="| grep my_filter"

would result in:

    `tail -f /usr/share/my_app/shared/log/my_env.log | grep my_filter`

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
