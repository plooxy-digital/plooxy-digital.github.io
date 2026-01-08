# AI & LLM Agent Instructions

This file serves as the definitive guide for AI agents and LLMs generating code and content for the **Plooxy Digital** static site repository.

## 1. Project Overview
This repository functions as a multi-tenant static site host (similar to Linktree). Each folder represents a distinct business entity containing its own landing page.
-   **Host**: GitHub Pages.
-   **Structure**: `/business-folder/` containing independent assets.

## 2. Directory Structure & File Standards
When creating a new business page, strictly follow this structure:

```text
business-name/
├── index.html   # Main entry point (Semantic HTML5)
├── styles.css   # Main stylesheet (Mobile-First)
└── images/      # Asset folder for logos/products
```

## 3. Workflow Protocol `[CRITICAL]`
Before writing any code, you must:
1.  **Analyze Request**: Identify the business type, target audience, and key goals.
2.  **Ask Follow-ups**: If the user hasn't provided specific details, ASK for:
    -   Business Name & Tagline.
    -   Brand Colors/Theme preferences.
    -   Link definitions (Services, Booking, Contact).
    -   Specific call-to-actions (e.g., "Book Now", "Call Us").
    -   And any other relevant business info.

## 4. Coding Guidelines

### HTML (`index.html`)
-   **DOCTYPE**: `<!DOCTYPE html>`
-   **SEO**:
    -   Title tag: `Business Name | Service Keyword | Location`
    -   Meta Description: ~160 chars, persuasive copy.
    -   Canonical URL tag.
    -   Open Graph (`og:title`, `og:image`, `og:description`) and Twitter Card tags.
-   **Semantics**: Use `<main>`, `<header>`, `<nav>`, `<section>`, `<footer>` appropriately.
-   **Schema.org**: MUST include a `<script type="application/ld+json">` block for `LocalBusiness` or `Organization`.
-   **Accessibility**: `alt` tags on all images, proper contrast ratios, aria-labels on icon-only buttons.
-   **Copywriting**: Professional, engaging, and conversion-oriented. No generic filler if possible; infer reasonable copy based on the business type.

### CSS (`styles.css`)
-   **Modernity**: Use CSS Variables (`--primary-color`, `--spacing-unit`) for easy theming.
-   **Layout**: Flexbox and CSS Grid are required. No floats for layout.
-   **Responsive**: Mobile-first media queries. Ensure 100% layout integrity from 320px to 4k.
-   **Reset**: specific, minimal box-sizing reset (`*, *::before, *::after { box-sizing: border-box; }`).
-   **Performance**: Avoid heavy framework imports (Bootstrap/Tailwind) unless requested. Stick to vanilla CSS for speed and simplicity.

## 5. Interaction Style (Vibe)
-   **Professional**: Be concise and expert.
-   **Inquisitive**: Don't guess wildly—ask for clarification on critical missing business info.
-   **High-Quality**: Treat every file as a production-ready deliverable.
