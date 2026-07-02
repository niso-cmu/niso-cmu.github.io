# NISO Website

Source for the NISO (Neuroscience Institute Student Organization, CMU) website, built with
[Jekyll](https://jekyllrb.com/) and deployed via GitHub Pages.

## Local development

```sh
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.

## Structure

- `_config.yml` — site-wide settings and shared links (join form, Slack, calendars, etc.)
- `_layouts/`, `_includes/` — page shell, header, footer
- `assets/css/style.css` — all site styling
- `index.md` — Home
- `about.md` — Mission/vision, board, past members, gallery
- `join.md` — Join form, Masters/PhD info, Slack, email lists, resources
- `guide/index.md` — New Student Guide (Tommy's guide)
- `calendars.md` — NISO / NI Outreach / CNBC calendars
- `projects.md` — Outreach, Data Clubs, Social events
- `wiki.md` — Link out to the NISO GitHub wiki

## Editing content

Most content lives in plain Markdown files with `<!-- EDIT ME -->` comments marking sections
that need real content. Edit directly on GitHub (use the pencil icon) or clone locally.

Shared links (Slack, calendar IDs, join form, etc.) are defined once in `_config.yml` under
`links:` — update them there rather than hunting through every page.

## Deployment

Pushing to `main` triggers `.github/workflows/pages.yml`, which builds the Jekyll site and
publishes it to GitHub Pages automatically. In the repo settings, set **Pages > Source** to
"GitHub Actions".
