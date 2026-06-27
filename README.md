# Sales BI Blueprint

A static, self-contained implementation of the **Sales-Focused BI Blueprint** —
a Power BI consulting deliverable for a premium imported meat & seafood
distributor in Vietnam (Wagyu-led, HORECA + retail).

The page is a scoping report that reads the client's `MASTERFILE` workbook and
lays out, end to end:

1. Sheet inventory & classification (facts, dims, targets, RLS, QA helpers)
2. The derivable executive / "Business Overall" view
3. Per-department read (Accounting/AR, Warehouse, product masters)
4. **Sales deep dive** — the lead deliverable (coverage matrix, KPI catalogue, opportunities & risks)
5. Data-quality issues with Power Query fixes
6. Recommended star-schema data model
7. Dashboard pages (Sales lead + Executive, AR, Warehouse)
8. Wireframes (client-ready B1 Sales Overview + structural sketches)
9. DAX measures (Sales-first, incl. the signature margin-leakage measure)
10. Power Query transformation recipe
11. Build priority (P1–P4)
12. Final recommendation + questions for the client

## Implementation

This was handed off from Claude Design as an HTML/CSS/JS prototype and rebuilt
here as a clean, dependency-free static site:

- `index.html` — semantic markup for the full 12-section document
- `styles.css` — all styling, extracted from the prototype's inline styles into
  reusable classes and CSS custom properties (palette, type scale, spacing)
- A small inline scrollspy script highlights the active section in the contents nav

Fonts (Space Grotesk, IBM Plex Sans, IBM Plex Mono) load from Google Fonts. The
layout is responsive and includes print styles (the nav collapses for print).

## Viewing

Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Notes

- All figures in the report are read directly from the source `MASTERFILE`
  workbook and are intended to be validated with the client.
- The original design tool's runtime (`support.js`) and the `<x-dc>`/`<helmet>`
  wrappers from the handoff bundle are scaffolding and are not part of this
  implementation.
