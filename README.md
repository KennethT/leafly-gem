# Leafly

Leafly API Gem.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'leafly'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install leafly

## Usage

Gem Setup
Insert the following code as a model in your rails app.
def initialize
  @leafly = Faraday.new(:url => 'http://data.leafly.com') do |faraday|
    faraday.request  :url_encoded             # form-encode POST params
    faraday.response :logger                  # log requests to STDOUT
    faraday.adapter  Faraday.default_adapter  # make requests with Net::HTTP
  end
end

Add .env to .gitignore file.  Then add to your .gitignore file:
APP_ID=Your_Leafly_ID
APP_KEY=Your_Leafly_Key






## Contributing

1. Fork it ( https://github.com/[my-github-username]/leafly/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request
