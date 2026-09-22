# Backlog

Standing queue of development work for this project, ordered by priority.
Created 2026-09-22.

**Status:** Shipped — public reading shelf, driven by [bibliotheca-archive](https://github.com/sheljustdoes/bibliotheca-archive)

---

## P0 — Shelf usability

`index.html` is 347 lines and renders `books.json` directly. It works; it does not yet
scale to a large shelf.

- [ ] Filter by status (reading / finished / want) — currently everything renders in one
      list.
- [ ] Sort by date finished, title, or author.
- [ ] Client-side search across title and author.
- [ ] Render ratings and notes where the sidecar JSON provides them; they are collected by
      the archive pipeline and never displayed.

## P1 — Presentation

- [ ] Cover art from the Google Books thumbnail already present in the metadata.
- [ ] Reading statistics: books finished per year, a simple pace line.
- [ ] Open Graph tags so a shared link previews properly.

## P2 — Quality

- [ ] Accessibility pass — semantic list markup, focus states, contrast in both themes.
- [ ] Verify layout at phone width.
- [ ] Graceful empty and error states for a missing or malformed `books.json`.

## Documentation

- [ ] Note in the README that the shelf is generated and should not be edited by hand —
      `books.json` is written by the archive repository's Action.
- [ ] Document the `books.json` schema, including which fields may be null.
