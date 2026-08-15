# TSANet Connect Developer Hub

Static developer portal for TSANet Connect members. Covers connectors, gateways, the REST API and SDK, the interactive design document library, and community topic areas (AI-focused problem resolution systems, CRM and ticketing modernization).

No build step, no framework, no external dependencies. Plain HTML and CSS, deployable as-is to GitHub Pages.

## Structure

```
index.html                  Portal landing page
assets/                     Brand assets (2025 identity)
  TSANet-icon_white_blue_512px.png            App tile icon (nav, footer, favicon)
  TSANet-Connect-Icon_2025_vertical_Transparent.png   Connect mark (hero)
  Blue_TSANet_icon.png                        Alternate icon (unused, reference)
docs/                       Design document library (add standalone HTML docs here)
```

## Brand tokens

All colors are defined once in the `:root` block of `index.html`, sampled from the 2025 brand assets:

| Token | Value | Use |
|---|---|---|
| `--blue` | `#005B82` | Petrol blue: nav, footer, primary text accents |
| `--cyan` | `#337C9B` | Steel blue: secondary elements |
| `--orange` | `#CC4E0B` | The single accent: primary button, headline emphasis, nav rule |
| `--ink` | `#093D56` | Body headings |

Orange is used sparingly by design, mirroring the single orange dot in the mark.

## Adding a design document

1. Drop the standalone HTML file into `docs/` (e.g. `docs/tsanet-2026-014-oauth-architecture.html`).
2. Add a card in the Design Document Library section of `index.html` pointing to it.

## Deploying to GitHub Pages

1. Push this repo to the `tsanetgit` org (e.g. `tsanetgit/developer-hub`).
2. Repo Settings > Pages > Deploy from branch > `main` / root.
3. Optional custom domain: `developer.tsanet.org` (add a CNAME record pointing to `tsanetgit.github.io`, then set the domain in Pages settings; GitHub provisions TLS automatically).

## Community layer (optional)

Discussion links point at GitHub Discussions in the tsanetgit org. To embed a discussion thread inline on any page (including design docs), add a [giscus](https://giscus.app) script block; it renders the mapped GitHub Discussion in place with no additional platform.
