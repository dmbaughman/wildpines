wildpines
=========

# Wild Pines Counseling
This is the professional website for Annie Flansburg-Spiess, a counselor for at-risk adolsecents in the Seattle area.  I wrote the site using Wok as a static HTML generator, because that produces un-hackable, fast-loading pages.  No dynamic content was needed for this site, so it lent itself toward using a static generator.

## Pre-requisites
To compile the source code for this site, you'll need to install [Wok](http://wok.mythmon.com) and all its prerequisites (Python, Jinja, Markdown, YAML).
I also used LESS to create a customized look for [Bootstrap](http://twitter.github.com/bootstrap), so if you need to make any CSS changes, get yer LESS compiler installed as well.
I did my development in Sublime Text, so there's a sublime-project that goes along with the source code; but you can use whatever text editor you want.

---

## Content
The page-specific files are [Markdown](http://daringfireball.net/projects/markdown/) files, but since I was using Bootstrap's grid, I wrote most of the content in HTML instead of true Markdown.

## Styles
I left the majority of the Bootstrap [LESS](http://lesscss.org/) files alone so future updates aren't a pain. The few changes I made are the following:
* Added custom.less file which is imported by bootstrap.less
* Added custom-responsive.less file which is imported by bootstrap-responsive.less
* Added/customized variables in the variables.less file

## Templates
Wok uses [Jinja](http://jinja.pocoo.org/docs/) templates (in the ./templates/ directory), so if anything needs to be changed to the base template, or any other templates for that matter, read up on yer Jinja.  It's pretty straightforward, especially if you've used any server- or client-side templating.

## Media
The ./media/ directory is where you put anything that needs to be compiled without a template, so here's where you put the images, scripts, compiled CSS, etc.  I used this as a place to put the PDF forms for the forms page.

## Pre-Compiled
This is where I put the LESS files, as well as any scripts before compiling/minifying them.  I ended up not doing my own minification for the JS plugins for Bootstrap, so this really is just for the LESS files.

## Output
Assuming that you're successful at making changes to the site, your final product will be in the ./output/ directory

## Other directories
The rest can be ignored because they're either not important (misc) or I didn't use them (hooks).

## Config
The site configuration, including site title and author.  These end up being site-level variables which are used in the Jinja templates to put the site title on each page and stuff.