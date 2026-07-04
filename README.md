# LingoTrail — Interface Prototype (UED100 Assessment 2)

A responsive front-end prototype built on the UX/UI analysis of a language-learning
web app (Assessment 1: Duolingo). This is an original interface — not a clone —
that applies the same interaction patterns identified in the analysis (tile-based
lessons, streak/XP gamification, persistent top navigation) while addressing the
accessibility gaps noted for keyboard and screen-reader users.

## How to view it
Open `index.html` in any modern browser. No build step or server required —
it is plain HTML/CSS/JS with no dependencies beyond a Google Fonts link.

## Folder structure
```
lingotrail/
├── index.html        Page structure and content
├── css/
│   └── style.css      Design tokens (CSS variables) + responsive layout
├── js/
│   └── script.js       Nav toggle, trail rendering, modal, form validation
└── README.md
```

## Interactive components
- **Responsive navigation** — collapses to a hamburger menu under 720px, with
  `aria-expanded` state kept in sync for screen readers.
- **Lesson trail** — rendered from a JS data array; clicking an unlocked lesson
  opens an accessible modal (focus is trapped/returned, Escape closes it).
- **Contact form** — client-side validation with inline error messages and a
  live-region status message on submit (no page reload).
- **Animated stats** — streak/XP counters and a progress bar animate on load,
  respecting `prefers-reduced-motion`.

## Accessibility notes (carried over from Assessment 1 findings)
Assessment 1 flagged that the original app was not fully smooth for keyboard
and screen-reader users. This prototype addresses that with: a skip-to-content
link, visible focus outlines on every interactive element, semantic landmarks
(`header`, `nav`, `main`, `section`, `footer`), `aria-live` regions for the
streak counter and form status, and a modal that manages focus correctly.
