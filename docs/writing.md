---
description: >
  Hydejack offers a few additional features to markup your content.
  Don't worry, these are merely CSS classes added with kramdown's `{:...}` syntax,
  so that your content remains compatible with other Jekyll themes.
hide_description: true
---

# Writing
Hydejack offers a few additional features to markup your content.
Don't worry, these are merely CSS classes added with kramdown's `{:...}` syntax,
so that your content remains compatible with other Jekyll themes.

**NOTE**: For an introduction to markdown in general, see [Mastering Markdown][mm] and [kramdown Syntax][ksyn].
{:.message}

## Table of Contents
{:.no_toc}
0. this unordered seed list will be replaced by toc as unordered list
{:toc}

## A word on building speeds
If building speeds are a problem, try using the `--incremental` flag, e.g.

    bundle exec jekyll serve --incremental

From the [Jekyll docs](https://jekyllrb.com/docs/configuration/#build-command-options) (emphasis mine):

> Enable the experimental incremental build feature. Incremental build only re-builds posts and pages that have changed, resulting in significant performance improvements for large sites, *but may also break site generation in certain cases*.

The breakage occurs when you create new files or change filenames.
Also, changing the title, category, tags, etc. of a page or post will not be reflected in pages
other then the page or post itself.
This makes it ideal for writing new posts and previewing changes, but not setting up new content.

## Adding a table of contents
You can add a generated table of contents to any page by adding `{:toc}` below a list.

Example: see above

Markdown:
~~~md
* this unordered seed list will be replaced by toc as unordered list
{:toc}
~~~

## Adding message boxes
You can add a message box by adding the `message` class to a paragraph.

Example:

**NOTE**: You can add a message box.
{:.message}

Markdown:
~~~markdown
**NOTE**: You can add a message box.
{:.message}
~~~

## Adding large text
You can add large text by adding the `lead` class to the paragraph.

Example:

You can add large text.
{:.lead}

Markdown:
~~~markdown
You can add large text.
{:.lead}
~~~

## Adding large images
You can make an image span the full width by adding the `lead` class.

Example:

![Full-width image](https://placehold.it/800x100){:.lead data-width="800" data-height="100"}

Markdown:
~~~markdown
![Full-width image](https://placehold.it/800x100){:.lead data-width="800" data-height="100"}
~~~

## Adding image captions
You can add captions to images by adding the `figure` class to the paragraph containing the image and a caption.

![Full-width image](https://placehold.it/800x100){:.lead data-width="800" data-height="100"}
A caption for an image.
{:.figure}

Markdown:
~~~md
![Full-width image](https://placehold.it/800x100){:.lead data-width="800" data-height="100"}
A caption for an image.
{:.figure}
~~~

For better semantics, you can also use the `figure`/`figcaption` HTML5 tags:

```html
<figure>
  <img alt="An image with a caption" src="https://placehold.it/800x100" class="lead" data-width="800" data-height="100" />
  <figcaption>A caption to an image.</figcaption>
</figure>
```

## Adding large quotes
You can make a quote "pop out" by adding the `lead` class.

Example:

> You can make a quote "pop out".
{:.lead}

Markdown:
~~~
> You can make a quote "pop out".
{:.lead}
~~~

## Adding faded text
You can gray out text by adding the `faded` class. Use this sparingly and for information that is not essential, as it is more difficult to read.

Example:

I'm faded, faded, faded.
{:.faded}

Markdown:
~~~md
I'm faded, faded, faded.
{:.faded}
~~~


[mm]: https://guides.github.com/features/mastering-markdown/
[ksyn]: https://kramdown.gettalong.org/syntax.html
[ksyntab]:https://kramdown.gettalong.org/syntax.html#tables
[ksynmath]: https://kramdown.gettalong.org/syntax.html#math-blocks
[katex]: https://khan.github.io/KaTeX/
[rtable]: https://dbushell.com/2016/03/04/css-only-responsive-tables/
