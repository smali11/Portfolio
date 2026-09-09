# Swapnil Mali — Portfolio

Personal portfolio site. Single self-contained `index.html`: no build step, no framework, no bundler.

**Live:** _add your URL after the first deploy_

## Stack

- Vanilla HTML/CSS/JS
- [Three.js](https://threejs.org) — hero environment (orbit rings, particles, lighting)
- [GSAP](https://gsap.com) + ScrollTrigger — scroll-driven animation
- [Lenis](https://lenis.darkroom.engineering) — smooth scrolling
- Fonts: Space Grotesk + Inter (Google Fonts)

Libraries load from CDN. The portrait and résumé are embedded in the HTML, so the page works even if `public/` is missing.

## Structure

```
index.html                 the whole site
public/Swapnil_Resume.pdf  résumé (also embedded in index.html)
```

## Run locally

```bash
python3 -m http.server 8000
# → http://localhost:8000
```

Open `index.html` directly if you prefer; everything is inline.

## Deploy

**Vercel** — import the repo, framework preset **Other**, leave build command empty, output directory `.`

**Netlify** — build command empty, publish directory `.`

**GitHub Pages** — Settings → Pages → Deploy from branch → `main` / root

## Sections

Hero · About (skills web) · Experience · Projects · AI + GenAI · System Design · Mindset · Tech Stack · Contact

## Notes

- The contact form uses `mailto:`, so it opens the visitor's mail client rather than sending server-side. For guaranteed delivery, wire it to Formspree or a serverless function.
- The hero is built so a real 3D character can replace the illustration: drop a GLB at `public/models/swapnil.glb` and the scene picks it up automatically.
- Accessibility: semantic headings, keyboard-navigable diagrams, and `prefers-reduced-motion` support throughout.

© 2026 Swapnil Mali
