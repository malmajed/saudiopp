# SaudiOpp — Saudi Arabia Investment Intelligence

**saudiopp.istawra.com** · by Istawra Consulting

105 PSAP investment opportunities across 11 Saudi strategic sectors, 2026–2035.

## Deployment

This is a static site deployed via Cloudflare Pages to `saudiopp.istawra.com`.

### GitHub → Cloudflare Pages setup

1. Push this repo to GitHub
2. In Cloudflare Pages: Connect to GitHub → select this repo
3. Build settings: none (static HTML, no build step)
4. Output directory: `/` (root)
5. Custom domain: `saudiopp.istawra.com`

### Cloudflare Access gate

In Cloudflare Zero Trust → Access → Applications:
- Application: `saudiopp.istawra.com`
- Policy: Email OTP — add approved emails to the allow list
- Public paths (no gate): `/` — sector grid and node cards are public
- Protected paths (require login): none yet — full briefs are behind the modal email gate

## Structure

```
index.html        — full static site, all 105 nodes embedded
README.md         — this file
CNAME             — custom domain for GitHub Pages (if using GH Pages instead)
```

## Content

All 105 PSAP nodes are embedded directly in `index.html` as JSON. No backend required.

Full briefs (when generated) will be added as individual JSON files and loaded dynamically.

## Contact

hello@istawra.com · istawra.com
