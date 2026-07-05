# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev      # start dev server (http://localhost:5173)
npm run build    # production build → dist/
npm run preview  # serve the dist/ build locally
```

No test suite is configured.

## Architecture

Vanilla JS + Vite static site. No framework, no component library.

- `index.html` — single-page HTML with all content (hero, about, services, contact, footer)
- `src/style.css` — all styles; uses CSS custom properties defined in `:root`
- `src/main.js` — minimal entry point; imports `style.css`, no app logic
- `vite.config.js` — sets `base: '/'` (required for GitHub Pages root URL compatibility)
- `public/` — static assets copied verbatim: `CNAME` (GitHub Pages domain), `.nojekyll`

Deployed to GitHub Pages via the `dist/` output.

## Brand / Design System

The approved brand lives in `Kappa Software Labs logo/`:

- **Logo mark**: three horizontal lines of unequal length with a teal dot — represents the κ symbol and Kappa architecture pattern
- **SVG assets**: `assets/kappa-tile-dark.svg`, `assets/kappa-tile-light.svg`, `assets/kappa-mark-mono.svg`
- **Colors**:
  - Dark background: `#10201F`
  - Teal primary: `#2FB5B3`
  - Teal dark: `#0E7C7B`
  - Paper/off-white: `#FCFBF9`
- **Typography**:
  - Wordmark: Space Grotesk 600
  - Tagline / monospace details: IBM Plex Mono 400, letter-spacing 0.27em
- **Full spec**: `Kappa Software Labs logo/Kappa Logo - Final.dc.html`

The `styleguide/` directory is currently empty — it is intended for future style documentation.
