# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Marketing landing page generator for dental practices built with Astro 5. Static site focused on lead generation and conversion-optimized pages.

## Commands

```bash
npm run dev      # Start dev server at localhost:4321
npm run build    # Build to ./dist/
npm run preview  # Preview production build
```

## Architecture

**Framework**: Astro 5 with TypeScript (strict mode)

**Routing**: File-based - create `.astro` files in `src/pages/` for new routes

**Components**: Astro components in `src/components/` with scoped `<style>` blocks. Props accessed via destructuring: `const { propName } = Astro.props;`

**Styling**:
- Global CSS with variables in `src/styles.css`
- Component-scoped styles using `<style>` blocks
- CSS nesting supported
- Brand color: `--brand: #0041ff`
- Fonts: Inter (body), Instrument Serif (headings) loaded from `/public/fonts/`

**Assets**: Place in `public/` directory, reference with `/` prefix (e.g., `/img/hero.webp`)

## Key Patterns

- Use `set:html={}` directive for rendering HTML content in props (see HeadingStack.astro)
- No framework islands (React/Vue/etc.) - pure Astro components only
- Components are small and single-purpose with scoped styling
