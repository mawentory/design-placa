# Placa — design reference

**Signage on drawing paper**

One page showing every component in this design, rendered from its own design
tokens. No build step, no dependencies: open `index.html`.

**[View the component gallery →](https://mawentory.github.io/design-placa/)**

![Placa](preview.png)

## What is here

| File | Purpose |
| --- | --- |
| `index.html` | Component gallery — every component on one page |
| `DESIGN.md` | The design notes: origin, palette, type, shape, measured contrast |
| `theme.css` | The 66 design tokens, plus derived accessibility values |
| `design.css` | Component styles, written against tokens only |
| `fonts.css` | `@font-face` declarations for the fonts this design uses |
| `fonts/` | Latin-subset woff2 files, self-hosted |

`design.css` contains no colour, radius or font literal. That is deliberate: the
same stylesheet drives all ten designs and only `theme.css` differs, so the
gallery doubles as a test that the token set is complete.

## The design

Brazilian road and wayfinding signage: amber signal paint on light grey drawing paper, chunky borders, and offset shadows that read like a painted board rather than a page.

**Type** — Overpass for text and Overpass Mono for numbers: both were drawn for signage and hold up at small sizes and low resolution. Headings run at 800 with tight negative tracking.

**Shape** — 10px radii on controls, 2px borders, and a hard 6px 6px 0 shadow. Depth comes from an offset, never from a blur.

**Signature moves**

- Hard offset shadows (`--shadow-card: 6px 6px 0`) instead of soft elevation.
- 2px borders on every surface, including inputs.
- Signal amber used once per view as the action colour.

## Colour

| Token | Value | Role |
| --- | --- | --- |
| `--paper` | `#e7ebe6` | Page ground |
| `--sheet` | `#f3f5f1` | Raised surfaces |
| `--ink` | `#142029` | Primary text |
| `--signal` | `#f2a007` | Action |
| `--signal-text` | `#905f04` | Action, when it has to be read |
| `--focus-ring` | `#b77905` | Focus indicator |

## Accessibility

Every colour pair this design can render as text is checked against WCAG 2.1
when the repo is generated — page surfaces, panel surfaces, and the tinted fills
of badges and diff lines. The full table is in
[DESIGN.md](DESIGN.md#contrast-measured); the gallery is separately audited in a
real browser for heading order, duplicate ids, unlabelled controls and
horizontal overflow at 1280px and 390px.

## Using it

Set the theme attribute on your root element and load the two stylesheets:

```html
<html data-theme="placa">
  <link rel="stylesheet" href="fonts.css" />
  <link rel="stylesheet" href="theme.css" />
  <link rel="stylesheet" href="design.css" />
</html>
```

Because the tokens are namespaced by attribute, this theme can sit alongside
another one in the same page.

## The rest of the set

[Blueprint](https://github.com/mawentory/design-blueprint), [Phosphor](https://github.com/mawentory/design-fosforo), [Press](https://github.com/mawentory/design-imprensa), [Swiss](https://github.com/mawentory/design-suico), [Neon](https://github.com/mawentory/design-neon), [Brutalist](https://github.com/mawentory/design-brutalista), [Botanical](https://github.com/mawentory/design-botanico), [Bauhaus](https://github.com/mawentory/design-bauhaus), [Vidro](https://github.com/mawentory/design-vidro).

---

Part of the MarvinRouter design set. Generated from a single template; see
`DESIGN.md` for the values behind it.
