# WHAM! BAM! DevLog!

The development home for **WHAM! BAM! HAM-HAM!**, the Card Brawler from WHAM! BAM! Studios. Built with [Zine](https://zine-ssg.io/) and deployed to GitHub Pages.

## Preview locally

From the repository root, run the bundled Zine server:

```powershell
.\zine.exe
```

Then open the local address printed by Zine. To build a production copy:

```powershell
.\zine.exe release
```

The generated site is written to `public/`.

## Publish

The workflow in `.github/workflows/deploy.yml` builds and deploys the site when changes are pushed to `main`. In the repository’s **Settings → Pages**, set the build and deployment source to **GitHub Actions**.

The Zine config is set up for this repository’s project-site URL: `https://whambamstudios.github.io/hamham/`.

## Theme

The site uses a Zine-compatible adaptation of the [Leap Day GitHub Pages theme](https://github.com/pages-themes/leap-day), with its banner, repository link, side navigation, and content layout implemented in `layouts/templates/base.shtml` and `assets/style.css`. `_config.yml` also selects `pages-themes/leap-day` for Jekyll; the current Pages workflow still builds with Zine, so the live appearance comes from the local Zine template and stylesheet.

## Add a DevLog entry

Create one dated page per update at `content/devlog/YYYY-MM-DD-short-title.smd`:

```smd
---
.title = "A short headline",
.description = "A one-sentence summary for the homepage, archive, and feed.",
.date = .date("2026-10-12T12:00:00"),
.layout = "post.shtml",
.tags = ["devlog", "CardBrawler"],
---

Write the update here.
```

The homepage automatically shows the five newest entries; the archive and RSS feed include every page tagged `devlog`, ordered by date. No separate homepage or archive edit is needed. Keep `content/devlog/YYYY.smd` for an optional year overview.

## WHAM! BAM! HAM-HAM! Player Guide

New to the game? Visit the [player guide on the live site](https://whambamstudios.github.io/hamham/guides/), which introduces the rules, campaign, side modes, cards, Heroes, and collection systems. Individual card text and in-game rules take precedence; mode availability can vary by build and server.

### Start here

- [First Match: Rules & Mechanics](https://whambamstudios.github.io/hamham/guides/getting-started/)
- [Campaign Mode](https://whambamstudios.github.io/hamham/guides/campaign-mode/)
- [Side Modes & Mini-Games](https://whambamstudios.github.io/hamham/guides/side-modes/)

### Cards & combat

- [Card Types](https://whambamstudios.github.io/hamham/guides/card-types/)
- [Elemental Aeon](https://whambamstudios.github.io/hamham/guides/elemental-aeon/)
- [Card Stats](https://whambamstudios.github.io/hamham/guides/card-stats/)
- [Card Mechanics & Rules](https://whambamstudios.github.io/hamham/guides/card-mechanics-and-rules/)
- [Hero Cards, Resolve & Limit Break](https://whambamstudios.github.io/hamham/guides/hero-cards/)

### Your collection

- [Collection Binder](https://whambamstudios.github.io/hamham/guides/collection-binder/)
- [Deck Builder](https://whambamstudios.github.io/hamham/guides/deck-builder/)
- [Trading & Auctions](https://whambamstudios.github.io/hamham/guides/trading-and-auctions/)
- [Sharding & Crafting](https://whambamstudios.github.io/hamham/guides/sharding-and-crafting/)

Aeon is temporary energy spent during a match; Elemental Shards are persistent collection currency between matches.
