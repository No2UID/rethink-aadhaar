# Rethink Aadhaar

[![Built with Astro](https://img.shields.io/badge/Astro-7-FF5D01?logo=astro&logoColor=white)](https://astro.build)
[![TypeScript strict](https://img.shields.io/badge/TypeScript-strict-3178C6?logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind v4](https://img.shields.io/badge/Tailwind-4-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com)
[![License: MIT](https://img.shields.io/badge/code-MIT-blue)](#license)
[![License: CC BY 4.0](https://img.shields.io/badge/content-CC%20BY%204.0-lightgrey)](https://creativecommons.org/licenses/by/4.0/)
[![Contribute via issues](https://img.shields.io/badge/contribute-via%20issues-brightgreen)](https://github.com/No2UID/rethink-aadhaar/issues/new)

The official website of [rethinkaadhaar.in](https://rethinkaadhaar.in) — a static, accessibility-first site built with Astro 7, Tailwind v4, and MDX content collections.

External pull requests are closed automatically; please [open an issue](https://github.com/No2UID/rethink-aadhaar/issues/new) describing the change instead.

## Quick start

Requires **Bun 1.3+** ([install](https://bun.sh/install)).

```sh
bun install
bun run dev          # http://localhost:4321
bun run build        # optimize-images + astro check + build + scripts
bun run preview      # serve dist/
bun run check        # Biome lint + format check
bun run fix          # Biome auto-fix (safe rules only)
```

## Adding content

The fastest way to add an update, exclusion story, or press entry:

```sh
bun run new -- update    "Statement on the latest exclusion incident"
bun run new -- exclusion "Aadhaar-linked pension denial in Khunti" --location "Khunti, Jharkhand"
bun run new -- press     "Headline" --publication "The Wire" --href https://example.com
```

New entries ship as `draft: true`. Flip the flag to publish. See [`TECHNICAL.md`](./TECHNICAL.md) for the manual workflow, or [`COLLABORATOR.md`](./COLLABORATOR.md) for the browser editor at `/admin/`.

## Project layout

```
src/
  lib/          Core utilities (single source of truth)
  content/      7 Zod-typed MDX collections
  components/   Astro components
  pages/        Route pages
  layouts/      BaseLayout.astro
  styles/       Global CSS / Tailwind config
scripts/        Build-time tools
```

## License

- **Code:** MIT — see [`LICENSE`](./LICENSE). Copyright © 2025-2026 Anivar Aravind.
- **Content** (`src/content/`): [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) by Rethink Aadhaar.
- **Press coverage:** title, outlet, date, and URL only; links to original publishers.
