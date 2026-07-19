# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Site Overview

Personal portfolio website for Joshua Teves, hosted on GitHub Pages at joshuateves.com. Built with Jekyll's minimal theme — no build pipeline, no dependencies, no npm. All pages are hand-written HTML with a single shared stylesheet (`style.css`). GitHub Pages handles deployment automatically on push to `main`.

## Development

There is no local build step required. To preview locally if Jekyll is installed:

```bash
jekyll serve
```

Otherwise, push to `main` and GitHub Pages will deploy automatically.

## Architecture

- **All pages** are plain `.html` files using inline HTML structure; there are no Liquid templates or Jekyll includes beyond the theme itself.
- **`_config.yml`** sets only the theme (`jekyll-theme-minimal`) and nothing else.
- **`style.css`** contains minimal overrides (font family: Book Antiqua) on top of the theme defaults.
- **Navigation** between pages is done with plain `<a href="...">` links — there is no shared nav component.

## Content Organization

| Directory / File | Purpose |
|---|---|
| `index.html` | About/biography page |
| `active_projects.html` / `inactive_projects.html` | Project listings |
| `blog_posts/` | Blog entries; `toc.html` is the table of contents |
| `books/` | Book reviews; `books_read.html` is the reading list index |
| `fun/` | Hobby pages (pens, dog pictures) |
| `quotes.html` | Quotes collection |

New content pages should follow the existing pattern: a standalone `.html` file in the appropriate directory, linked from the relevant index page (e.g., a new book review goes in `books/` and gets a link added to `books/books_read.html`).
