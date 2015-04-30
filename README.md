# Jekyll Webmention.io Supplements

Not everything we want comes via Brid.gy, so we can directly query services to find links to our posts and supplement the webmention.io results.

**Requires [jekyll-webmention_io](https://github.com/aarongustafson/jekyll-webmention_io).**

## Twitter

The `get_twitter_webmentions.rake` rakefile will search for your posts and pages via the Twitter Search API. You will need to [register your site as an app](https://apps.twitter.com/app/new) and acquire the necessary keys. Store them in the following environment variables:

* `TWITTER_CONSUMER_KEY`
* `TWITTER_CONSUMER_SECRET`
* `TWITTER_ACCESS_TOKEN`
* `TWITTER_ACCESS_SECRET`

You may need to update line 5 of the rakefile to point to your root folder. The current line assumes this rakefile is contained in `/tasks/rake/` and merged into your master Rakefile using

	Dir.glob('tasks/rake/*.rake').each {|r| load r}

## ToDo

* Facebook
* Google+