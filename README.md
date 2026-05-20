# Andrew Fuller's Personal Site

Personal website and blog built with [Quarto](https://quarto.org), hosted on [GitHub Pages](https://pages.github.com).

🌐 **Live site:** https://andrew-fuller.github.io

## Stack

- **Framework:** Quarto (blog + static site)
- **Hosting:** GitHub Pages (free)
- **CI/CD:** GitHub Actions — auto-deploys on every push to `main`
- **Styling:** Custom SCSS (light + dark mode)

## Local Development

1. Install [Quarto CLI](https://quarto.org/docs/get-started/)
2. Clone this repo
3. Run `quarto preview` to start a local dev server

## Writing a New Post

```bash
# Create a new post folder
mkdir blog/posts/my-new-post

# Create the post file
touch blog/posts/my-new-post/index.qmd
```

Add the front matter:

```yaml
---
title: "My Post Title"
description: "A short description."
author: "Andrew Fuller"
date: "2026-05-20"
categories: [R, Shiny]
---
```

Then `git push` — GitHub Actions handles the rest.

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml` which:
1. Sets up R + Quarto
2. Runs `quarto render`
3. Deploys the `docs/` folder to GitHub Pages
