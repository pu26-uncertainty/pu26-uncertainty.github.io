# PU26 Uncertainty Workshop Site

Public website for the **Energy Infrastructure Planning Under Uncertainty** workshop at PowerUp 2026 (full-day, September 11 2026, University of Colorado Boulder). Deployed via GitHub Pages at https://pu26-uncertainty.github.io.

## Stack

- **Jekyll** with the `mmistakes/minimal-mistakes@4.27.3` remote theme, `air` skin
- Site config: [_config.yml](_config.yml) (includes the top nav — `_data/navigation.yml` is present but unused)
- Plugins: `jekyll-remote-theme`, `jekyll-include-cache`

## Layout

- [index.md](index.md) — landing page: hero banner, nav cards, "workshop materials" callout
- [_pages/](_pages/) — content pages, all use `layout: single` via the default in `_config.yml`:
  - [overview.md](_pages/overview.md) — workshop motivation and goals
  - [agenda.md](_pages/agenda.md) — tentative schedule (markdown table)
  - [speaker-bios.md](_pages/speaker-bios.md) — keynotes, panel 1, panel 2, spotlights
  - [organizer-bios.md](_pages/organizer-bios.md) — organizing team
  - [materials.md](_pages/materials.md) — talk slides (files in [assets/slides/](assets/slides/)) plus related reading (Khorramfar et al. survey)
  - [faqs.md](_pages/faqs.md) — placeholder
- [_includes/footer.html](_includes/footer.html) — custom footer with PowerUp link
- [assets/css/main.scss](assets/css/main.scss) — site-wide overrides (gradient title, nav, table headers, hero buttons)
- [assets/images/speakers/](assets/images/speakers/), [assets/images/organizers/](assets/images/organizers/) — bio photos
- [assets/slides/](assets/slides/) — speaker slide decks, named `firstname_lastname.{pdf,pptx}`, linked from the Materials page

## Brand & conventions

- **Brand gradient:** `#a699cc` (purple) → `#f0a090` (peach). Reuse for any new visual elements — used in the site title, nav cards, paper callouts, table headers, and `.gradient-heading` sections.
- **Inline styles:** Each page repeats its own `<style>` block for shared patterns (`.paper-callout`, `.speaker`, `.organizer`, `.gradient-heading`, nav cards). Editing a visual pattern often means touching multiple files. If you change one, scan the others for the same selector.
- **Speaker/organizer cards:** 110×110px square images with `object-fit: cover` and `object-position: center top`. Bio photos go in `assets/images/{speakers,organizers}/`.
- **External links:** All `http(s)` links pick up the purple→peach hover styling via [assets/css/main.scss](assets/css/main.scss).

## Organizers

Most are MIT (Ana Rivera, Lara Booth, Rahman Khorramfar, Aron Brenner, Ruaridh Macdonald, Saurabh Amin, Priya Donti); Gabriel Mantegna is at Princeton. See [_pages/organizer-bios.md](_pages/organizer-bios.md) for current details.

## Editing tips

- Page front matter only needs `title:` and `permalink:` — layout defaults to `single` from `_config.yml`.
- Top nav is in `_config.yml` under `navigation:`, not in `_data/navigation.yml`.
- Tables auto-pick up the gradient header from [assets/css/main.scss](assets/css/main.scss).
- The site uses font-awesome icons (`<i class="fas fa-...">`) — these come from the theme's default header includes.
