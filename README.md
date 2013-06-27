# Ympfilter

Ympfilter means 'Yet another xmpfilter implementation'.
Xmpfilter is in a gem '[rcodetools](http://rubygems.org/gems/rcodetools)'.

It will be able to inject evaluated variable to the (hash rocket) comment.

For Example: foo.rb

```ruby
:a                              # =>
'foo'                           # =>
['a','b','c'].each do |e|
  e                             # =>
end
puts 'hello'                    # =>
```

`$ xmpfilter foo.rb`

```ruby
:a                              # => :a
'foo'                           # => "foo"
['a','b','c'].each do |e|
  e                             # => "a", "b", "c"
end
puts 'hello'                    # => nil
# >> hello
```

## Installation

Add this line to your application's Gemfile:

    gem 'ympfilter'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install ympfilter

## Usage

TODO: Write usage instructions here

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
