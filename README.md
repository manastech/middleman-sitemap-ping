# Middleman Sitemap Ping

[![Gem Version](https://badge.fury.io/rb/middleman-sitemap-ping.png)](http://badge.fury.io/rb/middleman-sitemap-ping)
[![Build Status](https://secure.travis-ci.org/bootstrap-ruby/middleman-bootstrap-navbar.png)](https://travis-ci.org/krautcomputing/middleman-sitemap-ping)

> ⚠️ **Deprecated**: since both [Bing](https://blogs.bing.com/webmaster/may-2022/Spring-cleaning-Removed-Bing-anonymous-sitemap-sub) and [Google](https://developers.google.com/search/blog/2023/06/sitemaps-lastmod-ping) killed their public sitemap-ping endpoints, this gem doesn't work anymore. This fork won't be maintained anymore.
>
> Don't use it.

[Middleman](https://middlemanapp.com/) extension to ping search engines (Google and Bing) with a sitemap URL

## Installation

Add this line to your application's Gemfile:

    gem 'middleman-sitemap-ping'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install middleman-sitemap-ping

## Versions

Use version 1.x of this gem for Middleman 4 or 0.x for Middleman 3.

## Usage

Activate the extensions in `config.rb` in your Middleman app:

```ruby
activate :sitemap_ping do |config|
  config.host         = 'http://www.mywebsite.com' # (required)                       Host of your website
  config.sitemap_file = 'custom-sitemap-file.xml'  # (optional, default: sitemap.xml) Name of your sitemap file
  config.ping_google  = false                      # (optional, default: true)        Ping Google?
  config.ping_bing    = false                      # (optional, default: true)        Ping Bing?
  config.after_build  = false                      # (optional, default: true)        Run automatically after build?
end
```

Once the extension is activated, it will ping the search engines automatically every time you build your site (unless you set `config.after_build = false`).

You can also execute the ping from the command line:

```
bundle exec middleman sitemap_ping
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## Support

If you like this project, consider [buying me a coffee](https://www.buymeacoffee.com/279lcDtbF)! :)
