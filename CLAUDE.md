# chuckallen.ai

## What this is
ChuckAllen.ai — AI/automation specialty arm under the ChuckAllen.dev parent brand. "A ChuckAllen.dev Company" appears on this site and mrwpress.com. Positioned as a practical engineering consultancy — NOT an "AI company." AI and automation are tools in the toolkit, not the identity. Avoid AI-hype language. Single-page scrollable model with anchor sections.

## Rules
- **Performance first** — every decision filtered through performance impact
- **No CSS frameworks** — all CSS is component-scoped via Astro `<style>` blocks
- **Single page model** — one `index.astro` with section components, anchor nav. Legal pages (privacy, terms) are the only separate routes.
- **Images in `src/assets/`** — always use `<Picture />` from `astro:assets` for AVIF + WebP
- **SVGs in `public/`** — they don't need processing
- **Never push to main** — always branch → PR → merge
- **noindex/nofollow** can be set per-page via the `noindex` prop (defaults to false)
- **TypeScript strict mode**, ESNext target
- **Shared components from `@mrwpress/shared`** — import BaseLayout, Header, Footer, Contact, etc.
- **Site config in `src/config/site.ts`** — single `SiteConfig` object, one source of truth

## Stack
- Astro (static SSG)
- Component-scoped CSS + shared design tokens
- Cloudflare Pages + Workers
- npm (public) for @mrwpress/shared

## Deployment
Merge to `main` triggers Cloudflare Pages rebuild.
