# Bordeaux Liquid Gold — events

The calendar and the two dinners, as static pages.

    /events                        index.html
    /events/chateau-palmer-2026    chateau-palmer-2026/index.html
    /events/cheval-blanc-2026      cheval-blanc-2026/index.html

Plus the three share cards the pages reference, and `sophie-entry/` — the snippet, CSS and
photograph that add the “Private dinners” link and band to Sophie's page.

## Publishing with GitHub Pages

Settings → Pages → Source: **Deploy from a branch** → Branch: `main`, folder: `/ (root)` → Save.

The site appears at `https://<username>.github.io/<repo>/events/` within a minute or two.
`.nojekyll` is included so Pages serves the folders as-is.

## Important: the share cards

`og:image` and `og:url` inside the pages are absolute and point at
`https://sophie.bordeauxliquidgold.com/events/...`. If this repo is served from a different
domain, those tags must be updated to match, or link previews will show a blank card.

## Updating

Replace the changed file, commit, and Pages redeploys. Every version is kept in history, so
rolling back is a matter of reverting a commit.

## Nothing here talks to a server

Each page carries its own CSS, fonts and photographs inline. The reservation form builds a
WhatsApp or email message in the visitor's browser and transmits nothing until the guest
presses send.
