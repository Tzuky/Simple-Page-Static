# IT Support Varna — Static Page

A simple, single-page static website for an IT support service based in Varna, Bulgaria.
Hosted free via **GitHub Pages**.

**Live site:** https://tzuky.github.io/Simple-Page-Static/

---

## About

Personal landing page for the services I offer locally:

- PC repair & diagnostics
- OS install / reinstall (Windows, Linux)
- PC upgrades (RAM, SSD, GPU, PSU)
- LAN setup & configuration
- NAS setup & configuration (Synology, QNAP, TrueNAS)
- On-site and remote support

No build step, no framework, no dependencies — just HTML, CSS and a bit of vanilla JS.

---

## Structure

```
.
├── index.html    # the entire site
└── README.md     # this file
```

Everything lives in `index.html` — styles are inlined in `<head>`, and the small
amount of JS at the bottom handles the scroll reveal animations, sticky nav state
and pointer-parallax on the ambient orbs.

---

## Deploying to GitHub Pages

Currently set to **Deploy from a branch** (`master` / root), so every push goes
live automatically — no Actions workflow needed.

To update the site, just edit and push:

```bash
git add .
git commit -m "Update site"
git push origin master
```

If Pages ever needs re-enabling:

1. Go to **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: **master** / **(root)**
4. Save, then wait ~1 minute for the build

---

## Images

Photos are currently hotlinked from Unsplash. To use your own, drop them into an
`images/` folder in the repo and replace the `src` values in `index.html`:

```html
<img src="images/nas-setup.jpg" alt="Synology NAS setup">
```

---

## Tech notes

- Dark theme with animated gradient mesh, glassmorphism cards and backdrop blur
- Scroll-reveal animations via `IntersectionObserver`
- `prefers-reduced-motion` is respected — all animation is disabled for users who
  have asked for it
- Fully responsive, down to small mobile widths

---

## Contact

- **Phone:** +359 888 123 456
- **Email:** support@itsupportvarna.bg
- **Location:** Varna, Bulgaria