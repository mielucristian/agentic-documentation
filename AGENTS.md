# AGENTS.md

Operating context for AI agents (the Framer 3.0 in-canvas Agent, and any coding/automation agent) working on the **Agentic** design-agency template.

> This file describes *how to work on the project*, not how to use it. For human-facing docs, see `README.md`.

---

## Project at a glance

- **Name:** Agentic
- **Kind:** Single-page Framer agency template (creative studio / design agency)
- **Live reference:** https://agentic.framer.website/
- **Owner / author:** UIHUB.DESIGN (Cristian Mielu)
- **Design language:** Bold, editorial, high-contrast. Parenthetical section labels — `(WORK)`, `(ABOUT US)`, `(SERVICES)`, `(AWARDS)` — and the `AGENTIC®` wordmark are part of the visual identity.

## Structure the agent should respect

Single scrolling page with anchored sections, plus standalone routes.

**Anchored sections (in order):**
`hero-section` → `work-section` → `about-section` → `services` → awards → `footer-background` (contact).

**Routes:**
- `/` — main page
- `/works` — project index
- `/works/{artikle|flowpath|kudos}` — case-study detail pages
- `/legal/privacy-policy`, `/legal/cookie-policy`, `/licensing`

**Repeating content models:**
- **Work items** — title, category, client, duration, cover image, link.
- **Team members** — name, role, tagline, photo, Twitter/LinkedIn links (carousel, 6 entries).
- **Awards** — date, title, description (reverse-chronological list).
- **Services** — heading + paragraph (6 entries).

## Conventions

- Preserve the parenthetical section-label style when adding or relabeling sections.
- Keep the `®` on the `AGENTIC` wordmark unless explicitly rebranding.
- Work, team, awards, and services are **structured, repeating** content — edit them as collections/items, not as one-off frames. Match existing field shapes when adding entries.
- Maintain responsive behavior; the template is mobile-ready and changes should not break smaller breakpoints.
- Section anchors are referenced by the nav. If you rename a section, update its anchor **and** every nav link pointing to it.

## Tasks the agent is likely asked to do

- Rebrand (wordmark, palette, type) without altering layout structure.
- Add / remove / reorder work items, team members, awards, or services.
- Add a new case-study detail page following the existing `/works/{slug}` pattern.
- Update contact details, booking link (Calendly), and social URLs.
- Edit legal pages.

## Guardrails — confirm before doing

- **Do not** alter or remove license-required attribution in the footer (`UIHUB.DESIGN`, "made in Framer") without explicit instruction; check `/licensing` first.
- **Do not** restructure the single-page layout into multiple pages, or vice versa, unless asked.
- **Do not** delete the existing work/team/award/service collections; edit in place.
- Treat any MCP connection credentials as **secret** — never echo, log, or embed them in output, components, or committed files.
- Placeholder data (e.g. `hello@agentic.com`, duplicated award blurbs, repeated social links) is intentional scaffolding — flag it for the user rather than inventing real replacements.

## Definition of done

A change is complete when: layout and responsiveness are intact, all nav anchors resolve, repeating content uses consistent field shapes, branding/attribution rules are honored, and no secrets appear anywhere in the project or output.
