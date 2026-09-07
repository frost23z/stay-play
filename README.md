# Eagle Creek Golf Club — Stay & Play Page

A raw HTML + CSS recreation of the provided design (desktop, tablet, and
mobile mockups), built with no frameworks.

## Overview of structure and approach

- **`index.html`** — one semantic page using `<header>`, `<nav>`, `<main>`,
  `<section>`, `<article>`, `<aside>` and `<footer>`. Each major block of the
  design (hero, nearby stays, highlights, reviews, course features,
  best-time-to-play/weather, other courses, footer) is its own `<section>`
  with a heading, so the outline reads correctly with screen readers and the
  heading hierarchy stays in order (one `<h1>`, then `<h2>` per section, then
  `<h3>`/`<h4>` inside cards).
- **`style.css`** — a single external stylesheet, organized in commented
  blocks: Reset → Variables → Layout → Utilities → Header → per-section
  styles → Media Queries. Layout uses **Flexbox** and **CSS Grid** only (no
  floats). Class names follow a light **BEM** convention
  (`.property-card__body`, `.btn--outline`, etc).
- **`assets/`** — images used in the project.

## Breakpoints used

- **Desktop:** default styles, 
- **Tablet — `max-width: 1024px`:** the header collapses to the hamburger
  menu, the hero's booking card stacks above the gallery, the property/stay
  layout drops the side-by-side map, and multi-column grids (highlights,
  reviews, seasons, other courses, footer links) step down to 2 columns.
- **Mobile — `max-width: 420px`:** the search field collapses to an icon,
  "BOOK A TEE TIME" collapses to an icon, side gallery thumbnails are hidden
  (main photo only), and all grids become a single column.

## Assumptions / limitations

- No JavaScript was used, per the assignment scope. Interactive-looking
  controls from the mockup (date pickers, filter dropdowns, the image
  carousel dots/arrows, map zoom/satellite toggle, pagination) are marked up
  as real, focusable form/button elements for accessibility and styled to
  match, but they don't carry behavior — clicking them doesn't change page
  state.