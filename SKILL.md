---
name: branded-svg-icons
description: >-
  Select and integrate single-color SVG icons into Astro sites using Heroicons
  or project-local SVGs. Applies existing brand or neutral colors only; never
  invents colors. Use when explicitly invoked to add, replace, or style icons.
disable-model-invocation: true
---

# Branded SVG Icons

## Objective

Add consistent, accessible, single-color SVG icons to Astro sites. Prefer real SVG markup over icon fonts or new dependencies.

## Workflow

1. **Inspect** — Framework (Astro-first), existing icon usage, CSS variables / brand tokens, naming patterns. Do not add a second icon system.
2. **Source** — Heroicons first, then project-local SVGs. Do not install packages unless neither exists and the user approves.
3. **Select** — Match semantic meaning and nearby icon style/weight. Do not pick by name similarity alone.
4. **Color** — One color only (`fill` or `stroke`, not both mixed; no multicolor). Prefer an **existing** project CSS variable or hex. Never invent brand colors; if unknown, ask or use a neutral already in the project. Choose the color for contrast against the parent section background.
5. **Integrate** — Prefer reusable `.astro` components for repeated icons; otherwise local SVG assets. Follow the project's layout.
6. **Validate** — Renders, size/alignment, correct single color, a11y, consistency with nearby icons.

## SVG rules

- Valid `viewBox`; keep proportions; strip unnecessary markup.
- Do not alter icon geometry unless required.
- Decorative (label nearby): `aria-hidden="true"`.
- Meaningful alone: provide accessible text (`aria-label` or visually associated label).

## Principles

- Inspect before implementing; reuse before installing.
- Never invent colors, icon sources, or license permissions.
- Ask before changing the existing design system.
