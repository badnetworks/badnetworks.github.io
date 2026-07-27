# bn_www — Pathproof marketing site

Static marketing site for **Pathproof**, the commercial service from badnetworks,
built on the open-source Pathrate measurement core. Naming rationale:
`docs/branding/naming.md`.

Domains: served at **badnetworks.net** (registered at Porkbun; the CNAME here).
**pathproof.net** is also ours — once DNS for it exists, point it at the same Pages
site's `www` host or an HTTP redirect to badnetworks.net; GitHub Pages takes one
custom domain per site.

## Contents

- `index.html` — the whole site. Single self-contained page: inline CSS, ~90 lines of
  vanilla JS that draw the hero chart (no chart library). Google Fonts (Archivo,
  JetBrains Mono) is the only external dependency.
- `CNAME` — `pathproof.net`; must ship with every deploy.
- `.nojekyll` — disables Jekyll processing.

## Before launch (placeholders to resolve)

1. **Early-access CTA** — both "Request early access" buttons currently point at
   https://github.com/Pathrate. Swap for the real signup/contact destination.
2. **Chart data** — the hero chart is illustrative (a synthetic 30-day path with a
   congestion incident). Replace with an export from a real measurement when one
   exists; the data arrays are at the top of the inline script.

## Design notes

- Dark-only, deliberately: the page borrows the environment of its buyer (a NOC).
- Chart palette `#1e8fd5` (capacity) / `#c67a22` (ADR) is validated for
  colorblind-safety and contrast against the panel surface; the incident red is a
  reserved status color, always paired with a label. If you rebrand, re-validate.
- The pathrate.org sister site is light, IBM Plex, single orange accent — the two
  sites are intentionally distinct identities with a shared subject.
