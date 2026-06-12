# Rich Williams — Film · Edit
A single-file portfolio site in the style of 4wide.jp: light, Swiss/Japanese minimalism with data-sheet detailing.

## Design system
- **Background** `#F0F0F0` · **Ink** `#050505` · **Secondary** `#303030` · **Hairlines** `#C5C5C5` · single red accent `#A80505`
- **Type** Instrument Sans (sans) + Instrument Serif italic (accent words) — free Google Fonts standing in for PP Neue Montreal / PP Fragment Glare
- **Grid** 12 columns desktop / 6 mobile, 20px gutters
- Parenthetical section labels — (About the practice), (Services), (Approach) — coordinates, timecodes and other annotation details

## Features
- Preloader — minimal progress ring with red dot and % counter
- **Time-on-site clock** top-left (the "record timer") counts up from 0:00
- Hero: the muted showreel playing full-bleed behind a light wash, with the time-on-site timer and a pulsing ● REC — Showreel ’23 tag (no headline; an invisible h1 keeps SEO/accessibility intact)
- Selected Work: scroll-driven showcase — a sticky cinematic frame on the left crossfades between the 4 selected works as their chapters scroll past on the right (01/04 counter + label annotations); separate 5-row Archive list below
- Every work opens in an on-site video player (YouTube embed in a lightbox) with a Watch-on-YouTube fallback link
- Page-wipe transitions on nav clicks — an ink panel sweeps up with the section name in serif italics
- Autoplaying muted showreel with REC badge — click for full-screen with sound (same lightbox player)
- Selected Photography — staggered editorial grid of 6 stills (Caoilfhionn Rose portraits, Matthew Halsall live & artwork, Ancient Infinity Orchestra), embedded directly in the HTML as optimised WebP (~570KB total, lazy-loaded) — fully self-contained, no image folder needed
- Clients marquee, mega footer with grouped lists, giant "R*o*lling" word, ↑ Top
- Smooth scroll (Lenis) + reveal animations (GSAP ScrollTrigger + CSS transitions), with reduced-motion and no-JS fallbacks

## Deploy (GitHub Pages)
1. Create a repo, e.g. `richfilmedit-site`
2. Upload `index.html` to the repo root — it's fully self-contained
3. Settings → Pages → Source: `main` branch, `/ (root)` → Save
4. Live at `https://<username>.github.io/richfilmedit-site/` in ~1 minute
(Or drag the file into Netlify Drop / Vercel for instant hosting.)

## Customising
Everything lives in one file:
- **Works/links**: edit the `SELECTED` and `ARCHIVE` arrays in the `<script>` block
- **Services**: `SERVICES` array
- **Clients marquee**: `CLIENTS` array
- **Colours**: CSS `:root` variables at the top
- **Showreel**: swap the `<video src>` URL in the Approach section
- **Photography**: edit the `PHOTOS` array in the script — each entry has a caption, an image source (currently embedded data URIs — you can swap any for a normal image URL or path), an annotation tag, and a ratio class: `r45` (4:5), `r32` (3:2), `r11` (1:1). Keep new images under ~1600px and export as WebP (quality ~80) for fast loads

The earlier dark "edit suite" version is preserved if you'd like it back — just ask.
