# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static website for [OpenFab](https://openfab.be) — a Brussels-based FabLab (est. 2012) at 158 Rue Gray, 1050 Ixelles. Deployed via GitHub Pages with the custom domain `openfab.be` (see `CNAME`).

## Local Development

No build step. Open `index.html` directly in a browser:

```bash
# Quick local server (Python)
python3 -m http.server 8000
```

## File Structure

- `index.html` — main site page (French)
- `gamelab.html` — GameLab sub-page
- `css/styles.css` — custom styles (Bootstrap 4.6 is loaded from CDN)
- `openfab.json` — machine-readable space metadata in [Maps of Making / SpaceAPI](https://wiki.hackerspaces.org/SpaceAPI) format
- `images/` — logos and visual assets

## Key Architectural Notes

- **No JavaScript framework** — plain HTML/CSS with Bootstrap 4.6 and Font Awesome 4 from CDNs.
- **`openfab.json`** follows the SpaceAPI/Maps-of-Making schema (`api_compatibility: ["15"]`). Fields like `memberOf`, `sdgs`, and `state.open` have constrained allowed values — check schema docs before editing.
- The site is in **French**; keep content additions in French unless a section is explicitly multilingual.
- Bootstrap grid and components are used for layout; avoid adding a second CSS framework.
