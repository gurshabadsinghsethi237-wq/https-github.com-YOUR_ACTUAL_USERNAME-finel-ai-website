# Finel AI Website

Source repo for the finel.ai marketing site.

## Known technical SEO issues to fix (from live-site audit, 2026-07)

- Every route serves an identical `<title>`, meta description, and
  `<link rel="canonical">` (all pointing at the homepage) — service pages
  like `/tax`, `/t1tax`, `/bookkeeping` are being canonicalized away.
- No SSR/prerendering — `<div id="root">` is empty in the raw HTML, so
  crawlers that don't execute JS see no content.
- Unknown routes return HTTP 200 with homepage content instead of a 404.
