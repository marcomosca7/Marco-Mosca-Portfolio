# Tagline — Portfolio Site Notes
## Marco Mosca · Copywriter · New York

---

## Site Identity
- **Publication name:** TAGLINE
- **URL:** marcomosca7.github.io/Marco-Mosca-Portfolio
- **Custom domain (pending transfer):** marco-mosca.com
- **Hosted on:** GitHub Pages
- **Repo:** github.com/marcomosca7/Marco-Mosca-Portfolio

---

## Design System

### Colors
- `--bg: #f0ece3` — cream (light pages: homepage, Tubi, Whiskas, Home Depot)
- `--bg-dark: #0e0e0e` — near black (dark pages: Nike, Duolingo, Roomba)
- `--ink: #111010` — black text (light pages)
- `--ink-dark: #f0ece3` — cream text (dark pages)
- `--muted: #8a8680` — grey for captions, credits
- `--red: #c0392b` — accent red
- `--rule: rgba(17,16,16,0.15)` — light rule lines (light pages)
- `--rule-dark: rgba(240,236,227,0.12)` — light rule lines (dark pages)

### Fonts
- **Display:** Bebas Neue (headers, brand names, nav, TOC)
- **Serif:** Libre Baskerville (body copy, captions, italics)
- Both loaded via Google Fonts

### Spacing
- Page padding: `80px` left/right on campaign pages (images and text)
- Homepage broadsheet padding: `48px` left/right
- No full-bleed images — all images have 80px side margins on inline-styled pages

---

## Homepage (index.html)

### Layout
- Sticky masthead: Marco Mosca · Copywriter (left) | TAGLINE (center) | Work · About · X-Factor (right)
- Dateline: auto-updates daily via JS — "New York, N.Y. · [Day, Month Date, Year] · Est. 1995"
- Headline: `'ENTERTAINMENT' STOCKS PLUMMET AS PUBLIC DEMANDS MORE ADS` ("MORE ADS" in red)
- Byline: "By Marco" + parenthetical, right-aligned
- Broadsheet grid: `1fr 1fr 1fr 220px` columns
- TOC sidebar: sticky, col 4, spans all rows
- Footer: Bernbach quote (left) | "A Tagline Publication · © [dynamic year]" (right)

### Grid Layout (rows)
- Row 1: Nike (cols 1-2, wide lead) | Tubi (col 3) | TOC (col 4, sticky)
- Row 2: Duolingo (col 1) | Whiskas (cols 2-3, wide — mirrors row 1) | TOC continues
- Row 3: Roomba (cols 1-2, wide) | Home Depot (col 3) | TOC continues

### GIF Behavior
- Nike starts in full color on load
- All others start grayscale with sepia tint
- On hover: hovered image goes full color + slight scale
- When non-Nike is hovered: Nike reverts to grayscale

### GIF Filenames (all in repo root)
- Nike → `STILLCOUNTS.gif`
- Tubi → `TUBI.gif`
- Duolingo → `DUOMODE.gif`
- Whiskas → `WHISKAS.gif`
- Roomba → `ROOMBA.gif`
- Home Depot → `HOMEDEPOT.gif`

### Article Copy (exact)
- Nike: (New York, NY) Nike Moves the Unmoved Generation. / As idealistic advertising draws eye rolls... cont'd pg. 6
- Tubi: (Flyover, USA) Crop Circles Leave Americans Smug, Confused, Intrigued. / Streaming giant Tubi remains suspiciously silent... cont'd pg. 8
- Duolingo: (Our Heads, Rent Free) Duolingo Creates Unforgettable Reminder / Despite the success... cont'd pg. 11
- Whiskas: (Search Results, The Internet) Cat Food Brand Turns Typos to Traffic / Despite Whiskas... cont'd pg. 15
- Roomba: (Hardwood Floors, Home Interiors) Robot Reprograms, Redecorates / It's not the robot takeover... cont'd pg. 19
- Home Depot: (Young Homeowners, Just Kidding) Young Renters Find Aesthetic & Economic Relief in DIY / As costs continue... cont'd pg. 22

### TOC Credits & Page Numbers
- Nike: CW: Marco · AD: Marco · Pg. 6
- Tubi: CW: Marco · AD: Lauren T, Nick A, Annie Y. · Pg. 8
- Duolingo: CW: Marco · AD: Grecia R. · Pg. 11
- Whiskas: CW: Marco · AD: Fiona H. · Pg. 15
- Roomba: CW: Marco · AD: Christina C. · Pg. 19
- Home Depot: CW: Marco · AD: Lauren T, Nick A. · Pg. 22

### Pending
- Rotating headlines on return visits (sessionStorage) — Marco to write alternate headlines

---

## Campaign Pages

### Background Order (FINAL)
- Nike → DARK
- Tubi → LIGHT
- Duolingo → DARK
- Whiskas → LIGHT
- Roomba → DARK
- Home Depot → LIGHT

### Shared Structure (all pages)
- Ticker (black bar, scrolling campaign names)
- Sticky masthead: Marco Mosca · Copywriter (left) | TAGLINE (center, fades out on scroll) | Work · About · X-Factor (right)
- Campaign header: big brand name (clamp 5rem–11rem) + brand logo top right
- Intro copy block (wide, max-width 1200px)
- Executions with 80px side margins (no full-bleed)
- Closing line (italic, centered, wide margins — 240px on Tubi and Duolingo)
- Credits (Art Direction — Full Names)
- Prev/Next/Home nav (sticky at bottom, unsticks before footer via IntersectionObserver)
- Footer: Bernbach quote | "A Tagline Publication · © 2026"

### TAGLINE Scroll Behavior
JS hides TAGLINE from masthead once user scrolls past campaign header. Reverts on scroll back up.

### Prev/Next/Home Nav
- All 6 pages have a centered "Home" button between prev and next
- Nav is sticky at the bottom of the viewport
- Unsticks when the footer comes into view (IntersectionObserver)
- Nike and Tubi have this fully implemented with inline JS
- Duolingo has this fully implemented with inline JS

### Art Direction Credits (full names)
- Nike: Art Direction — Marco Mosca
- Tubi: Art Direction — Lauren Trujillo, Nick Alfonso, Annie Ye
- Duolingo: Art Direction — Grecia Rivera
- Roomba: Art Direction — Christina Chen
- Whiskas: Art Direction — Fiona Henne
- Home Depot: Art Direction — Lauren Trujillo, Nick Alfonso

### Page Numbers (FINAL — swapped Whiskas/Roomba)
- Nike: Pg. 6
- Tubi: Pg. 8
- Duolingo: Pg. 11
- Whiskas: Pg. 15
- Roomba: Pg. 19
- Home Depot: Pg. 22

### Nav Links
- Nike: no prev | Home | next → tubi.html
- Tubi: prev → nike.html | Home | next → duolingo.html
- Duolingo: prev → tubi.html | Home | next → whiskas.html
- Whiskas: prev → duolingo.html | Home | next → roomba.html
- Roomba: prev → whiskas.html | Home | next → home-depot.html
- Home Depot: prev → roomba.html | Home | no next

---

## Campaign-Specific Notes

### Tubi
- Transmission Error video embedded (not autoplay, with controls): `originals/tubi/Tubi- Transmission Errorcopy.mp4`
- Phase 01 text: "We touched down with the classic ET communication method of choice: crop circles."
- Phase 02 text: line break before "assuring them..."
- Phase 03 text: "Can you blame..." on its own line (br tag)
- Tubi lockup image at 60% width, centered, below closing line
- Crop circle images use object-fit: cover to match heights

### Duolingo
- DuoMode lockup image comes BEFORE "The Idea" section
- Idea description sits directly above the two app execution images (side by side)
- OOH executions are full-width (each its own img-full)
- Closing line centered with 240px padding

### Nike
- Duplicate old version removed (was appended after </html>)

---

## Brand Logos
- Nike: https://upload.wikimedia.org/wikipedia/commons/a/a6/Logo_NIKE.svg (working)
- Tubi: https://upload.wikimedia.org/wikipedia/commons/8/87/Tubi_logo_2022.svg (404 — needs replacement)
- Duolingo: needs working URL or local upload
- Whiskas, Roomba, Home Depot: not yet added

---

## Image Assets
- Campaign images currently hosted on Squarespace CDN
- Original source files backed up in `originals/` folder, organized by campaign
- `Book Point Two/` folder contains working files and assets from local development
- GIFs are in the GitHub repo root
- **Important:** Before canceling Squarespace, verify all images are accessible from GitHub

---

## Repo Structure
```
Marco-Mosca-Portfolio/
├── index.html          — Homepage
├── nike.html           — Nike campaign (inline dark styles)
├── tubi.html           — Tubi campaign (inline light styles)
├── duolingo.html       — Duolingo campaign (inline dark styles)
├── whiskas.html        — Whiskas campaign (style.css, light)
├── roomba.html         — Roomba campaign (style.css + dark override)
├── home-depot.html     — Home Depot campaign (style.css, light)
├── style.css           — Shared styles for Whiskas/Roomba/Home Depot
├── NOTES.md            — This file
├── *.gif / *.jpg / *.png — Homepage GIFs and shared assets
├── originals/          — Source image files by campaign
│   ├── nike/
│   ├── tubi/
│   ├── duolingo/
│   ├── whiskas/
│   ├── roomba/
│   └── home-depot/
└── Book Point Two/     — Local working files and assets
    ├── assets/         — GIFs organized by campaign
    ├── files working/  — Current HTML/CSS working copies
    └── files/          — Older HTML versions
```

---

## Pending Work
- [ ] Fix Tubi and Duolingo logo URLs (Wikipedia 404s — upload to repo or find alternatives)
- [ ] Add logos to Whiskas, Roomba, Home Depot pages
- [ ] Make Whiskas, Roomba, Home Depot sticky nav + footer observer (currently only Nike/Tubi/Duolingo have this)
- [ ] About page
- [ ] X-Factor page (bowling apparel personal project — "Don't Bowl Ugly")
- [ ] Domain transfer: Squarespace → Namecheap → point to GitHub Pages
- [ ] Download all Squarespace images before canceling account
- [ ] Rotating homepage headlines (sessionStorage) — write alternate headlines first

---

## Marco's Voice & Copy Notes
- Bold, simple, rhythm-driven. Humor is seasoning not the main course.
- Never sound like AI or generic copy.
- Sales-to-copywriter pivot is a core differentiator.
- Approach line: "Strategic enough to work, creative enough not to be boring."
- "Try-hard" is the worst possible outcome.
- Sensitive to anything generic, corporate, cold, or timid.
