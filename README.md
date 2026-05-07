# FL Sign Ops · Field Console

Private campaign field-ops dashboard. Hosted on Cloudflare Pages with Cloudflare Access (email auth) gating all routes.

## Deployment

This repo deploys as a static site. Cloudflare Pages serves `index.html` at `/`.

- `index.html` — main dashboard
- `sign_candidates_map.html`, `sign_status_map.html` — Folium-rendered map iframes referenced from the dashboard
- `_headers` — Cloudflare Pages applies these HTTP headers to all routes (anti-indexing, anti-clickjacking)
- `robots.txt` — second layer of search-engine-indexing prevention

## Access

Cloudflare Access policy gates the entire `*` route. Allowed identities are configured in the Cloudflare Zero Trust dashboard.
