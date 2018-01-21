# WoodInterface

 Just I was bored. Wooden Interface without methods of Class.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'wood_interface'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install wood_interface

## Usage

```ruby
module BaseInterface
  include WoodInterface

  methods do
    required_method :get_data
    required_method :set_data, key: String, data: ''
  end
end

module DataInterface
  include WoodInterface

  methods do
    required_method :data
    required_method :to_json
  end
end

class DataBase
  prepend BaseInterface
  prepend DataInterface

  def get_data
    ...
  end

  def set_data(data)
    ...
  end

  def data
    ...
  end

  def to_json
    ...
  end
end
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/[USERNAME]/wood_interface. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## License

The gem is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).

## Code of Conduct

Everyone interacting in the WoodInterface project’s codebases, issue trackers, chat rooms and mailing lists is expected to follow the [code of conduct](https://github.com/[USERNAME]/wood_interface/blob/master/CODE_OF_CONDUCT.md).
