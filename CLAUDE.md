# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a single-page landing site for Ugoki, a well-being and human performance platform. The entire site is contained in a single `index.html` file with embedded CSS and JavaScript - no build process, dependencies, or package management required.

## Architecture

**Single-File Structure**: All HTML, CSS, and JavaScript are contained in `index.html`. This includes:
- Embedded CSS in `<style>` tags (lines 10-800)
- Inline JavaScript at the bottom (lines 1113-1148)
- No external dependencies except Google Fonts

**Design System**: The site uses a light, pastel color palette defined in CSS custom properties (`:root` variables):
- Primary colors: Mint (`--color-mint`), Yellow (`--color-yellow`), Peach, Lavender
- Typography: Bebas Neue (display), Space Grotesk (body)
- Light theme with soft, monochromatic aesthetics

**Key Sections**:
1. Fixed navigation bar with survey CTA
2. Hero section with animated gradient orbs
3. Stats bar
4. Features grid (16 core features)
5. How It Works (3-step process)
6. Testimonials
7. Final CTA section
8. Footer

## Common Tasks

**Preview the site**: Simply open `index.html` in a web browser. No server required.

**Deploy changes**: This site is deployed via GitHub at https://github.com/linardsb/ugoki-lp.git on the `main` branch.

**Make content changes**: Edit `index.html` directly. All content, styling, and behavior is in this single file.

**Update the color scheme**: Modify CSS custom properties in the `:root` selector (lines 17-39).

**Adjust layout/spacing**: Look for padding values in section classes (`.hero`, `.features`, `.how-it-works`, etc.).

## Important Patterns

**Survey Integration**: The primary CTA throughout the site links to a Google Form: `https://forms.gle/ocmBM8NiT5eLuZnQ6`

**Animation System**:
- Scroll-based reveal animations using `.reveal` class
- Intersection detection via JavaScript (lines 1114-1128)
- Smooth scroll for anchor links (lines 1131-1139)

**Responsive Design**: Uses CSS Grid with media queries at 640px, 768px, and 1024px breakpoints.

**Semantic HTML**: Proper heading hierarchy is important for this site (h1 → h3 → etc). The hero subtitle specifically uses an h3 tag.

## Content Notes

- Footer copyright year is 2026
- Application is marketed as "coming soon" / under development
- Primary goal is survey participation to shape product features
- Non-functional footer links (Privacy Policy, Terms) have been removed
