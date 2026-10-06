# Marios Kalantzis — Portfolio

A Matrix-inspired, animated personal portfolio built with vanilla **HTML, CSS and JavaScript** (plus three.js for the 3D scene). No frameworks, no build step.

**Live:** https://marioskalantzis.github.io/PortfolioV2/

![Performance](https://img.shields.io/badge/Lighthouse_Performance-98-brightgreen)
![Accessibility](https://img.shields.io/badge/Accessibility-100-brightgreen)
![Best Practices](https://img.shields.io/badge/Best_Practices-100-brightgreen)
![SEO](https://img.shields.io/badge/SEO-100-brightgreen)

## Lighthouse

Measured on the live site (Lighthouse, headless Chromium).

| Category | 🖥️ Desktop | 📱 Mobile |
|----------------|:----------:|:---------:|
| Performance    | 98         | 96        |
| Accessibility  | 100        | 100       |
| Best Practices | 100        | 100       |
| SEO            | 100        | 100       |

**Core Web Vitals (mobile):** FCP 1.0s · LCP 2.7s · TBT 70ms · CLS 0.007

## Features

- Matrix digital-rain background (2D canvas) and a rotating wireframe icosahedron with a particle field (three.js), with mouse parallax and scroll-driven camera zoom
- Glitch hero title, typewriter role text and a terminal-style navigation
- Scroll-reveal sections, a scroll-progress bar and 3D tilt-on-hover project cards
- A hidden terminal easter egg (footer hint or the Konami code: ↑ ↑ ↓ ↓ ← → ← → B A)
- Downloadable CV, a contact section and project links

## Performance & accessibility notes

- Respects `prefers-reduced-motion` and pauses animation when the tab is hidden
- three.js initialises on `requestIdleCallback`, so WebGL never blocks first paint; WebGL failures fall back to the rain background
- Icons are an inline SVG sprite (no render-blocking icon font); the web font loads without blocking render
- Images are compressed, lazy-loaded and sized to avoid layout shift
- Keyboard-focus styles, a `<noscript>` fallback and an Open Graph social card

## Tech stack

HTML5 · CSS3 · Vanilla JavaScript · three.js

## Run locally

It is a static site — no build step. Serve the folder with any static server, for example:

```bash
npx serve .
```

Then open the printed `localhost` URL.

## License

© Marios Kalantzis. All rights reserved.
