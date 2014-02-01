# 6.813/6.831 Lecture Notes
These lecture notes are written in [Markdown](http://daringfireball.net/projects/markdown/syntax), a lightweight form of markup that compiles to a subset of HTML tags, and the static site is generated with [Jekyll](http://jekyllrb.com/), a static blog generator. The lecture note content (so far) has been scraped from PDFs available on the Spring 2013 Stellar. Styling is written in [Sass](http://sass-lang.com/), a CSS pre-processing language that provides handy features like variables and nesting.

## Running a copy locally
1. Install [Jekyll](http://jekyllrb.com/):

...   
~ $ gem install jekyll
...

2. Clone this repo.

...
~ $ git clone git@github.com:conniehuang/813lectures.git
~ $ cd 813lectures
...

3. Start the Jekyll server.

...
~ $ jekyll serve --watch --baseurl ''
...

The --watch flag auto-regenerates the site locally every time a change is made to source.
The --baseurl flag is necessary to get links working properly on localhost.

## Adding a new lecture
1. Create a new Markdown file in `_posts/`. The title must have the format:

...
YEAR-MONTH-DAY-title.markdown
...

The title should contain the lecture number (e.g., `L01`) and the short name of the lecture (e.g., "usability").
For more information, read the [Jekyll docs](http://jekyllrb.com/docs/posts/) on creating posts.
//TODO (carolynz): Write more!

## Making changes to the styling
If you are making changes to the styling, make sure to only edit the `.scss` file. Changes to the `.css` file will get overwritten when the `.scss` file recompiles. 

1. Make sure you install [Sass](http://sass-lang.com/).
2. Open up a new terminal window, cd to the `813lectures` directory, and enter:

...
~ $ sass --watch css/main.scss:css/main.css
...

This makes sure that any changes made to the `.scss` file are automatically reflected in the compiled `.css` file.

## File structure

...
//TODO (carolynz): write more!
...

### _layouts
Contains the templates for the entire site (`default.html`) and for each post (`post.html`).

### _posts
Contains all markdown posts.

### _site
Contains the compiled static site. Automatically gitignore'd.

### assets
Contains images, PDFs, other static assets.

### css
Contains `.scss` and compiled `.css` files.