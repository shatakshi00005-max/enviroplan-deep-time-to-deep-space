# Enviroplan — Deep Time to Deep Space

An immersive, scroll-driven brand experience for **Enviroplan**, a planetary restoration
company working across forests, oceans, and orbit. The site narrates a journey through
time — from an ancient Earth in balance, through the age of extraction, to a present-day
carbon-credit marketplace and the orbital-debris crisis above us — ending on a call to
**Restore. Reclaim. Renew.**

🌍 **Live:** https://enviroplan-deep-time-to-deep-space.vercel.app

---

## Experience

Ten full-viewport, scroll-snapped scenes with cinematic transitions:

1. **Hero** — interactive photoreal 3D Earth (Three.js) + hyperspace starfield
2. **The Jurassic** — cross-fading cinematic landscape footage with drifting embers & pollen
3. **The Collapse** — geological strata, an asteroid streak, "the age of extraction"
4. **Present Earth** — live planetary strain metrics (CO₂, orbital debris, forest loss, temp)
5. **Programs** — Ground Restoration / Carbon Marketplace / Orbital Debris, over looping footage
6. **The Ascent** — sky-to-space gradient with Earth curvature and atmosphere glow
7. **Orbital Reality** — a live canvas field of tracked LEO debris orbiting Earth
8. **The Marketplace** — a trading-desk UI with a live ticker and holographic credit cards
9. **Cosmic Scale** — a procedurally generated spiral galaxy with Earth as a pale blue dot
10. **Resolution** — a slow auto-rotating Earth, the mission statement, and footer

Plus a glowing pill nav, fixed scene-dot navigation, cinematic film grain + vignette,
3D card tilt with iridescent sheen, and full mobile/responsive layouts.

## Tech

- **Pure static site** — no build step. Open `index.html` and it runs.
- **Three.js** (r128, CDN) — photoreal Earth globes with cloud shells, fresnel atmosphere,
  and modeled satellites; planet textures from `threejs.org`.
- **Canvas 2D** — galaxy, orbital-debris field, hyperspace starfield, and ember particles.
- **Claude Design runtime** (`support.js`) — renders the design's `<x-dc>` template and the
  `Component` logic class. React is loaded by the runtime from a CDN.
- Fonts: **Fraunces**, **Plus Jakarta Sans**, **JetBrains Mono** (Google Fonts).

## Run locally

Any static file server works (a server is needed so the runtime can `fetch` the page and
the video assets):

```bash
npx serve .
# or
python3 -m http.server 8000
```

Then open the printed URL.

## Structure

```
index.html        # the design (10 scenes + Component logic)
support.js         # Claude Design runtime
image-slot.js      # image-slot custom element (loaded by the design; unused here)
uploads/           # the 4 referenced background video clips
vercel.json        # static hosting + asset cache headers
```

## Credit

Designed in [Claude Design](https://claude.ai/design) and implemented as a production
static site. Concept & contact: Shatakshi · Enviroplan.
