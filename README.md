Bridgy ![Bridgy](https://raw.github.com/snarfed/bridgy/master/static/bridgy_logo.jpg)
===

Got a blog? Share your blog posts on social networks? Wish comments on those
shared posts also showed up on your blog? Bridgy copies them back for you.

http://brid.gy/

_Bridgy is currently under construction._ I've recently updated it to use
[webmentions](http://www.webmention.org/) instead, so that it's a part of
the [IndieWeb](http://indiewebcamp.com/) ecosystem. I'm still debugging and
polishing it, though, so I don't recommend you use it just yet. Stay tuned!

License: This project is placed in the public domain.


Development
---
All dependencies are in git submodules. Be sure to run
`git submodule init; git submodule update` after you clone the repo.

The tests require the App Engine SDK and python-mox.


Related work
---
* http://webmention.io/
* https://github.com/vrypan/webmention-tools
* http://indiewebcamp.com/original-post-discovery
* http://indiewebcamp.com/permashortcitation
* http://indiewebcamp.com/Twitter#Why_permashortcitation_instead_of_a_link


TODOs
---
* only handle public posts. (need to add privacy/audience detection to
  activitystreams-unofficial?)
* cache some API calls with a short expiration, e.g. twitter mentions
* cache webmention discovery
* cache served MF2 HTML and JSON with a short expiration. ideally include the
  cache expiration in the content.
* global s/comment/reply/
* detect updated comments and send new webmentions for them
* store and render last N polls and propagates for each source
* likes/favorites. based on http://indiewebcamp.com/like and
  http://indiewebcamp.com/responses, it looks like it's just u-like and a
  webmention, similar to a reply and may not even need a u-in-reply-to.
  http://indiewebcamp.com/irc/2013-11-11 , http://indiewebcamp.com/repost
* allow deleting sources if you log in as them
* flesh out this readme
* clear toast messages
* use relative timestamps (moments ago, 4h, yesterday) when rendering recent
  comments
