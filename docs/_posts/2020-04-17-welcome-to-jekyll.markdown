---
layout: post
title:  "Welcome to my blog"
date:   2020-04-17 09:11:20 +1200
categories: [blog, update]
tags: [jekyll, github]
---
**This is my first posting with Jekyll, Wahoo!**

I did not have a wonderful experience installing it however. The [Jekyll website][jekyll-home] claims that you can _"Get up and running in seconds."_ but I took a couple of hours to get to hello world. So this first post is about that.

There where quite a few problems, some of my own making, however it was little things that tripped me up. For example when setting up the now Jekyll instance you need to use `_` either side of the version number else it will fail with an error *"Could not find gem 'github-pages (~> 3.8.5)' in any of the gem sources listed in your Gemfile."* This is not made clear in [githubs guide for creating pages with jekyll][creating-a-github-pages-site-with-jekyll] that recommends the command-line:
{% highlight bash %}
$ bundle exec jekyll VERSION new .
# Creates a Jekyll site in the current directory
{% endhighlight %}

This is the actual command-line that needs to be run is:
{% highlight bash %}
$ bundle exec jekyll _3.8.5_ new docs/
{% endhighlight %}

It also seems that a couple of extra steps in the deployment are required. Like when I bundle installed Jekyll I also had to bundle update after changing over to using github-pages Gem as for some reason it had Jekyll version 3.8.6 defined and not version 3.8.5 that I had installed.

Alls well that ends well however and I might even put a pull request in for the `_VERSION_` issue as it seems that this would be an easy improvement to GitHub's documentation.

[jekyll-home]: https://jekyllrb.com/
[creating-a-github-pages-site-with-jekyll]: https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll
