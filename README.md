# Chuanglan

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'chuanglan'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install chuanglan

## Usage

### Config

```ruby
Chuanglan.username  = 'username'
Chuanglan.password  = 'password'
Chuanglan.signature = '【签名】'

Chuanglan::International.username  = 'international_username'
Chuanglan::International.password  = 'international_password'
Chuanglan::International.signature = '【签名】'
```

### Send SMS

```ruby
Chuanglan.send_to!('10086', '流量唔够用啊')
Chuanglan.send_to!(['10086', '10010'], '信号好差啊')
Chuanglan.send_to!('10086', '流量唔够用啊', un: 'un', pw: 'pw', rd: 0, ex: 'ex', signature: '【覆盖签名】')
```

### Check balance

```ruby
Chuanglan.balance # => 100
```

### Send International SMS

```ruby
Chuanglan::International.send_to!('8613612345678', '流量唔够用啊')
Chuanglan::International.send_to!('8613612345678', '流量唔够用啊', un: 'un', pw: 'pw', dc: 15, rf: 1, tf: 3, signature: '【覆盖签名】')
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`. To release a new version, update the version number in `version.rb`, and then run `bundle exec rake release`, which will create a git tag for the version, push git commits and tags, and push the `.gem` file to [rubygems.org](https://rubygems.org).

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/GaiaMagic/chuanglan. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](contributor-covenant.org) code of conduct.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).

