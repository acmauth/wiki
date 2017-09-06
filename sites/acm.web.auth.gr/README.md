# Chapter's Website

The chapter main website is a [Jekyll](https://jekyllrb.com/) based website, hosted on [Github pages](https://pages.github.com/).

Jekyll is a lightweight publishing platform, which eliminates the need of a database. It has proven to be secure and flexible so far. On the downside, login and state is not offered to visitors.

## DNS

An A-record exists from acm.web.auth.gr to acmauth.github.io. This is configured in [hosted.auth](https://hosted.auth.gr/).

## Website hosting

The code of the website is publicly available at [Github](https://github.com/acmauth/acmauth.github.io).

In case you need to launch the project to your own computer, for preview purposes per se, you can:

* Clone the project
* Provided you have ruby and jekyll installed, run `jekyll serve` from the project top-level directory.

## Adding a post

In order to add a post, just add a new html, or md (aka Markdown) under the `_posts` directory. The name of the new file shoud adhere to the following standard:

```
YYYY-MM-DD-title-of-event.{md,html}
```

That is the full date, delimited by `-`, and the title of the event, also delimited by `-`.

For instance, an event called "Introducing Jekyll" to be held on 03/10/2017, will have the following filename:

```
2017-10-03-Introducing-Jekyll.md
```

### Post outline

```Markdown
---
layout: post

# Event information
title: "Introducing Jekyll"
cover: "../assets/introducing-jekyll/cover.png"
date: 2017/10/03
start_time: "11.00"
end_time: "16.00"

# Organizer
organiser: "Bob"
---

Post here
```

The first part, inside the `---` is called front matter, and specifies various information about the post itself. For events, we are using the `layout: post`.
For the post's cover, we are using the directory: `assets/name-of-event/cover.png`. In the same directory, we are saving all the relevant to the event files.

Last, you can add the name of the organiser. This part is optional, but adds contact info for the organiser to the post itself, plus their picture.

## Organizers

The organisers is a list of names, described in `_data/organisers.yml`. Simply append the already existent information for the person you want to add.

## Pages

For adding pages, you can use the `layout: page` line in the front matter.
We are adding all the pages in the top level directory of the project.
