# TripMod Bassic v1.0 — User Manual

Live: **https://rgr-audio-ee.github.io/tripmod-manual**

Bilingüal manual (ES/EN) for the TripMod Bassic v1.0 analog effects pedal.
Auto-detects browser language on first visit. Manual toggle button always visible.

## Structure

```
tripmod-manual/
├── index.html        ← Main document (all 17 pages, ES/EN)
├── assets/           ← All images (web-safe filenames)
│   ├── logotipo-tripmod.png
│   ├── logo-rgr.png
│   ├── foto-portada-1.png
│   ├── ph-fl-tr-analog-effects.png
│   ├── front-panel-phaser.png
│   ├── front-panel-flanger.png
│   ├── front-panel-tremolo.png
│   ├── panel-conectores.png
│   └── block-diagram-white.png
└── README.md
```

## GitHub Pages Setup

1. Go to repository **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / `/ (root)`
4. Save — URL will be `https://rgr-audio-ee.github.io/tripmod-manual`

## Updating the Manual

The source of truth is:
`D:\CUBANO\PEDALES\PROYECTOS\EFECTOS\MODULACIONES\PFT\User Manual TripMod\docs\TripMod_Manual_Completo.html`

After editing the source HTML, regenerate `index.html` with the transform script
(see firmware repo: `TripMod_bassic_v1.0` → `docs/` folder for instructions).

Key rules:
- Image paths in index.html use `assets/` prefix (web-safe filenames, no spaces)
- Language toggle: `localStorage` key `tripmod-lang` = `"es"` or `"en"`
- Do NOT add `class="lang-es"` or `class="lang-en"` hardcoded to `<body>` — JS sets it

## Deploying an Update

```bash
# From this repo root:
git add index.html assets/
git commit -m "docs: update manual vX.X.X"
git push origin main
```

GitHub Pages deploys automatically within ~1 minute of push.

## QR Code

QR points to: `https://rgr-audio-ee.github.io/tripmod-manual`

Files: `assets/qr-tripmod-manual.svg` and `assets/qr-tripmod-manual.png`
(Generated after GitHub Pages URL is live and confirmed.)

---

Firmware: TripMod Bassic v1.7.7 | RGR Effects & Electronic Engineering
