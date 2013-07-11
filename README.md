# Asset Precompilation in Rails 4

## Quick Guide

Notes to be aware of

in **config/production.rb**

make sure

````
config.serve_static_assets = true
```

Then the standard process means you can

````
RAILS_ENV=production rake assets:clobber

RAILS_ENV=production rake assets:precompile

RAILS_ENV=production rails s
````

Should mean you can test locally the precompiled assets.

For paths you can use...

with SCSS

````
background: image-url('test-image.png');
````

or even with ERB

````
background: url(<%= asset_path 'image-test.png' %>);
````

bear in mind there is no slash at the beginning.

## Full Guide

Clone this repo to see this in action.