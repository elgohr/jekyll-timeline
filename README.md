# jekyll-timeline

This is a small group of html and css includes for Jekyll that lets you create a beautiful timeline. It doesn't have any dependencies or require any plugins so it works great with out-of-the box Jekyll on GitHub Pages. I've tested it on Jekyll `3.3.0` and I'm personally motivated to make sure it stays functional with the [version GitHub uses](https://pages.github.com/versions/).

## Use Cases

This wasn't built to stagger overlapping timeframes, so it works best for use cases that are naturally non-overlapping, such as:

* Places you and your family have lived
* Heads of state like presidents and other world leaders
* Vehicles you've owned
* Major technology releases by manufacturer
* Star Trek Seasons, Ships, and Captains
* Star Wars films

## Features

* Hover for start and end dates, and to see event duration
* hover timeline background to see which year/month it represents
* Support for markdown inside timeline events, so you can include links and formatting
* Click to focus an event (partial solution for overlapping events and those events with long description content)

## Example Gallery

Minimal Configuration:

<a href="http://www.simple.gy/jekyll-timeline/example-minimal/">
<img src="https://github.com/SimplGy/jekyll-timeline/raw/master/_screencaps/simplegyjekylltimelineexampleminimal-clipped.png"/>
</a>

Five Columns:

<a href="http://www.simple.gy/jekyll-timeline/five-col/">
<img src="https://github.com/SimplGy/jekyll-timeline/raw/master/_screencaps/simplegyjekylltimelinefivecol-clipped.png"/>
</a>

Star Trek TV Series and Movies:

<a href="http://www.simple.gy/jekyll-timeline/star-trek/">
<img src="https://github.com/SimplGy/jekyll-timeline/raw/master/_screencaps/simplegyjekylltimelinestartrek-clipped.png"/>
</a>

My Resume Timeline:

<a href="http://simple.gy/resume/pretty">
<img src="https://github.com/SimplGy/jekyll-timeline/raw/master/_screencaps/simplegyresumepretty-clipped.png"/>
</a>

Share your examples with me by creating an issue with a link to how you've used this. I'd love to extend this to show some of the awesome things people have created.

## Running Locally

You can run this repo locally to explore the examples and play around with the options.

To run this project, start it like you would any Jekyll site. eg:

    bundle exec jekyll serve -w

## Installation

To use this project on your own sites, you can follow these steps.

[Create a Jekyll Site](https://jekyllrb.com/docs/quickstart/) (skip this if you already have one):

    ~ $ gem install jekyll bundler
    ~ $ jekyll new myblog
    ~ $ cd myblog
    ~/myblog $ bundle exec jekyll serve

Include the source files:

1. Cloning this project or downloading the [`_includes`](https://github.com/SimplGy/jekyll-timeline/tree/master/_includes) folder
2. Copy those files into your project's `_includes` folder

Reference the Dependencies:

1. include the css, either by moving `jekyll-timeline.css` into your `css` folder, or by using a [SASS import](http://sass-lang.com/guide)
2. Create a small example (the fastest way is to [copy mine](https://github.com/SimplGy/jekyll-timeline/tree/master/_posts) at first)
3. Customize by following the examples I've provided in the [`_posts`](https://github.com/SimplGy/jekyll-timeline/tree/master/_posts) folder

Use on your page:


<!-- {% include jekyll-timeline.html
   startYear=2010
   # This is a date near the oldest event you arere interested in showing. The timeline always runs up until now

   timelineHeight=600
   # Adjust this height until it fits your events comfortably

   col1Title="Minimal Example"
   col1Events=page.exampleEvents
%} -->

## Key Benefits

* No Jeykll plugins needed (this is why you can use it with GitHub Pages)
* No JavaScript at all, so it's easy to customize
* Prints almost pixel perfect (webkit only. Thanks to [`-webkit-print-color-adjust`](https://developer.mozilla.org/en-US/docs/Web/CSS/-webkit-print-color-adjust))

## Limitations

* No JavaScript at all, so UI interactions are limited (but you can easily add the behaviors you want)
* Timeline is always vertical
* Timeline always has most recent at the top
* No overlapping times (you can, but they aren't visually handled. They just occlude one another)
* Works on a 1mo granulary, so if your timeline spans 100s of years the hash marks may get too dense, and if it only spans a year or so the hash marks are too sparse. 

## Similar Projects

* [timeline-jekyll-theme](https://github.com/kirbyt/timeline-jekyll-theme) is a whole site theme rather than a reusable component. Might be a good fit if you like the vertical bubble style and have sparse events.

## Screenshot config

    webkit2png http://simple.gy/jekyll-timeline/five-col/ --width=1000 --clipwidth=250 --clipheight=150

