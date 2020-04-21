# heroku-deployment

We are going to work on a heroku deployment

Got this from:
https://gist.github.com/wh1tney/2ad13aa5fbdd83f6a489

This is a quick tutorial explaining how to get a static website hosted on Heroku.

**Why do this?**

Heroku hosts *apps* on the internet, not static websites. To get it to run your static portfolio, personal blog, etc., you need to trick Heroku into thinking your website is a PHP app. This 6-step tutorial will teach you how.

## Basic Assumptions

- You want to deploy some straight-up HTML, CSS, JS, maybe a few images. Nothing fancy here.
- You are in the root directory of your site (i.e. the directory that contains all subdirectories and files for the site)
- The root directory contains a main HTML page, e.g. index.html
- A [Heroku app](https://devcenter.heroku.com/articles/quickstart) and remote are set up and ready to go


## Steps

1. Add a file called *composer.json* to the root directory by running `touch composer.json`
2. Add a file called *index.php* to the root directory by running `touch index.php`
3. Rename the homepage (e.g. index.html) to *home.html*
4. In *index.php*, add the following line: `<?php include_once("home.html"); ?>`
5. In *composer.json*, add the following line: `{}`
6. Run `git push heroku master`

Done! Visit your deployed single-page website, hosted by Heroku (as a fake PHP app ☺).