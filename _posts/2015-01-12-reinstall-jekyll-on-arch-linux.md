---
layout: post
title: "Reinstall Jekyll on Arch Linux"
---

My desktop pc seems to be broken, so I had to do daily work on my small notebook ([ASUS X102BA](http://www.asus.com/Notebooks_Ultrabooks/X102BA/)). I reinstalled Jekyll on my notebook.

(1) Install Ruby.

```
$ sudo pacman -S ruby
$ gem install bundler
```

(2) Clone my github pages blog repository.

```
$ git clone git@github.com:fd3s/fd3s.github.io.git
$ cd ~/work/fd3s.github.io
$ ~/.gem/ruby/2.2.0/bin/bundle install
```

(3) Run a local web server.

```
$ ~/.gem/ruby/2.2.0/bin/bundle exec jekyll serve --drafts
```

**fd3s.github.io/Gemfile**

```
source 'https://rubygems.org'
gem 'github-pages'
```