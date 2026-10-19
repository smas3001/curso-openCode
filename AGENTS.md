# 01-demo

Simple HTML/CSS/JS learning page for exploring OpenCode. npm for deps, Tailwind v4 via PostCSS. No test runner, no bundler.

## Quick start

```bash
open index.html
```

## Build

```bash
npm run build:css   # input.css -> styles.css (run after editing HTML classes or input.css)
npm run dev:css     # watch mode
```

## Stack

- Vanilla HTML, CSS, JS in `index.html`
- Tailwind CSS v4: `input.css` (`@import "tailwindcss"` + `@source "./index.html"`) compiled to `styles.css` by `postcss.config.js` (`@tailwindcss/postcss` + `autoprefixer`)
- No `tailwind.config.js` -- v4 uses CSS-first config; content is auto-scanned from `index.html`
- `styles.css` is a committed build artifact so `open index.html` works without building

## Conventions

- README is in Spanish, code comments/commits can be in either language
- Single-page app - all work happens in `index.html`
- After adding/removing Tailwind classes in `index.html`, run `npm run build:css`
