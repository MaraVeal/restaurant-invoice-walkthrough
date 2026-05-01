# How to Read a Restaurant Invoice

An interactive, page-by-page walkthrough of a Fooda restaurant invoice — built as a training tool for new employees.

**Live site:** https://yourusername.github.io/invoice-walkthrough/  
*(replace with your actual GitHub Pages URL once it's live)*

## What it does

Click any of the three invoice pages and a zoomed view opens with numbered markers placed directly on the invoice. Click a marker — the relevant area highlights and a plain-language explanation appears beside it. No bullet-point side panels, no skimming. The invoice teaches you how to read it.

The three pages covered:

- **Page 1 — Summary.** Top-line numbers, the events table, and the deposit confirmation.
- **Page 2 — Event Invoice.** Card payments minus the four fee lines, line by line.
- **Page 3 — Reconciliation.** Sales side and Payments side, both landing on the same Gross Food Sales total.

A glossary of every term you'll see on a real invoice sits at the bottom of the page.

## How to use it

Open `index.html` in any modern browser, or visit the live link above. Works on desktop and mobile. No build step, no dependencies to install — it's a single self-contained HTML file.

## Editing the content

All hotspot text lives in the `PAGES` object near the bottom of the `<script>` block in `index.html`. Each hotspot has a `title`, a `body`, and an optional `tip`. Edit the strings, commit, and GitHub Pages will rebuild within a minute.

To add a new hotspot to a page, append an object to that page's `hotspots` array and make sure the `zone` value matches an `id` somewhere in that page's invoice HTML. The marker will position itself automatically next to the matching element.

## Tech notes

Pure HTML, CSS, and vanilla JavaScript. The only external dependency is Google Fonts (Fraunces + Geist) loaded over the internet. If served from a network that blocks Google Fonts, typography falls back to system fonts — still readable, just less polished.
