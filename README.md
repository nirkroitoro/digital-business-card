# Digital Business Card

A personal digital business card built with **HTML and CSS only** (no JavaScript). The site presents profile information, experience, skills, projects, and contact details in a clean, responsive layout with a CSS-only light/dark theme toggle.

## Live preview

Open [`index.html`](index.html) in any modern web browser. No build step or server is required.

## Features

- **Profile header** — name, role, area of expertise, and photo
- **About** — introductory paragraph covering background, interests, and completed projects
- **Additional sections** — background, interests, experience, skills, and projects
- **Contact** — GitHub, LinkedIn, phone, and email links
- **Light / dark mode** — toggle button implemented with a checkbox, `:has()`, and `color-scheme` (CSS only; preference resets on page reload)
- **Responsive layout** — mobile-first design with breakpoints for phones, tablets, desktops, and large screens
- **Accessibility touches** — semantic HTML, focus styles, and reduced-motion support

## Project structure

```
digital-business-card/
├── index.html          # Main page
├── style.css           # All styling (external stylesheet)
├── images/
│   └── profile.jpeg    # Profile photo
└── README.md
```

## Technical notes

### HTML & CSS only

The assignment requires HTML and CSS without JavaScript. Theme switching uses:

- A hidden checkbox inside the theme toggle label
- CSS `:has(#theme-toggle:checked)` to invert the active palette relative to the system preference
- `light-dark()` and CSS custom properties for separate light and dark color schemes

### Offline-first colors and styling

All colors are defined as CSS custom properties in `style.css`— light and dark palettes on `:root`, then mapped to semantic tokens (for example `--color-surface`, `--color-text`) using `light-dark()`. Nothing is loaded from a CDN: no Google Fonts, no icon packs, no external stylesheets. Typography uses the system font stack already available on the device.

This keeps the project fully usable **without an internet connection** — you can open `index.html` locally and develop, preview, and submit the same way everywhere. It also gives developers full control in one file: adjust a palette value once and the whole theme updates consistently, with no network dependency, no build step, and no third-party service that might change or go offline later.

## Browser support

Tested in current versions of Chrome and Safari. Theme toggle relies on modern CSS (`:has()`, `light-dark()`). Use an up-to-date browser for the full experience.

