# Universal Orlando — Family Itinerary

A styled, self-contained itinerary site for a family-of-7 Universal Orlando trip, **June 15–20, 2026** (Cabana Bay Beach Resort). Hosted on GitHub Pages.

**Live:** https://lastminute73.github.io/universal-studios/

## What's here

The homepage is a **gallery** to pick between three rebuilt designs. Each is one self-contained `index.html` (inline CSS/JS, Google Fonts via CDN) — the single source of truth to edit.

| Path | Design | Feel |
|---|---|---|
| [`/`](https://lastminute73.github.io/universal-studios/) | **Gallery** | Pick-a-design landing page |
| [`/design-1-timeline/`](https://lastminute73.github.io/universal-studios/design-1-timeline/) | **Live Trip Tracker** | Warm vertical timeline, live "you are here" status, crew chips |
| [`/design-2-magazine/`](https://lastminute73.github.io/universal-studios/design-2-magazine/) | **Travel Magazine** | Editorial print dispatch, serif headlines, print-friendly |
| [`/design-3-dashboard/`](https://lastminute73.github.io/universal-studios/design-3-dashboard/) | **App Dashboard** | Dark, app-style day tabs + live filters (crew / meals / Oz height) |
| [`/original/`](https://lastminute73.github.io/universal-studios/original/) | **Original** | The previous ticket-stub site, preserved unchanged |

## How each page is built (the edit surface)

All content lives in a JavaScript `DAYS` array near the bottom `<script>`. Each day is an object:

```js
{ id, dow, date, park, short, accent /* hex park color */, badges:[…], slots:[[time, htmlText, optionalClass]], alert }
```

`slots` = the hour rows; the optional 3rd value is `"meal"`, `"key"`, or omitted. To change a day, edit its object — don't touch the CSS or render code.

## Promoting a design to the homepage

Pick a favorite, then copy its `index.html` over the root `index.html` (keep the gallery around if you like — e.g. as `/gallery.html`). Pages redeploys in ~1 min.

## Trip facts baked into every design

- **Party of 7:** Zach, Becca, Grandma (62), Jace 14 (no coasters), Avia 12, Oz 4 (43"), Elowen 1 (no ticket).
- **Tickets:** 5-Day Park-to-Park for all 6 over age 3; 2-day Express Thu + Fri (everyone but Grandma); Express never at Volcano Bay, single-use per ride at Epic.
- **Add-ons:** 2 interactive wands (bought Mon), 3 Power-Up Bands (activated Thu).
- **Dining:** $600 hotel-only credit ($300 × 2 rooms), must be spent by Friday night; park lunches mobile-ordered ~20 min ahead.
