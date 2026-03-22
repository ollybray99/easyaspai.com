# Easy As AI — Claude Code Project Guide

## Project overview
This is the website for **Easy As AI** (easyaspai.com), a service that helps individuals and organisations learn and use artificial intelligence without the jargon.

The site is a **static HTML/CSS website** hosted on **GitHub Pages**. There is no build step, no framework, and no package manager — just plain HTML and CSS.

## File structure

```
index.html   — The entire single-page website (all content lives here)
style.css    — All styles; brand colours are defined as CSS variables in :root
CNAME        — GitHub Pages custom domain config — DO NOT edit or delete this
README.md    — Human-friendly editing guide for non-developers
images/      — Drop images here and reference them in index.html
```

## Tech stack
- Plain HTML5 and CSS3 — no JavaScript frameworks
- No build tools, no npm, no bundlers
- Deployed automatically via GitHub Pages on every push to `main`
- Custom domain: easyaspai.com (configured via CNAME)

## Brand colours (defined in style.css :root)
- Primary: `#6c3fc5` (purple)
- Accent: `#f5a623` (amber — used for buttons and highlights)
- Background: `#f7f5ff` (light lavender)
- Text: `#2d2d2d`

## Fonts
- Headings: Georgia (serif)
- Body: Arial (sans-serif)

## Conventions and guidelines
- All content for the page is in `index.html`. Each section has an HTML comment label (e.g. `<!-- HERO -->`, `<!-- ABOUT -->`) to make navigation easy.
- Keep everything in a single `index.html` unless the user asks to add new pages.
- CSS changes should use or extend the existing `:root` variables where possible.
- Do not add external JavaScript libraries or CSS frameworks unless specifically requested.
- Do not add a `.gitignore`, `package.json`, or any other tooling files — this is intentionally a zero-dependency project.
- Images go in the `images/` folder and are referenced relatively (e.g. `src="images/photo.jpg"`).
- The site is mobile-responsive; maintain responsiveness in any CSS changes.

## Common tasks
- **Edit content**: find the relevant comment block in `index.html` and edit the text
- **Change colours**: update the hex values in the `:root` block in `style.css`
- **Add a photo**: place the image in `images/`, then replace the grey placeholder `<div>` in the About section with an `<img>` tag
- **Add a new section**: copy an existing `<section>` block in `index.html` and adapt it; add a matching nav link in the `<header>`
- **Add a new page**: create a new `.html` file in the root, following the same header/footer structure as `index.html`

## Deployment
Changes go live automatically when pushed to the `main` branch on GitHub. No build or deploy step is needed.
