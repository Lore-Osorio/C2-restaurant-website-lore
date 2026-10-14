# Delicious Eats — Responsive & Accessible Restaurant Website

Refactor of a non-responsive, poorly accessible restaurant website into a modern, responsive and accessible site.

**Live site:** https://lore-osorio.github.io/C2-restaurant-website-lore/

## Improvements

### 1. Responsive design
- Replaced the float layout (`index.html`) and the table layout (`menu.html`) with **CSS Grid**: one column on mobile, two columns from 850px.
- Navigation uses **Flexbox**: links stack vertically on mobile and sit in a row from 600px.
- Mobile-first **media queries** at 600px (tablet) and 850px (desktop).
- Replaced the fixed `width: 800px` with `max-width`, and made all images fluid (`max-width: 100%; height: auto`).
- Added the **meta viewport** tag to both pages.

### 2. Accessibility
- Meaningful `alt` text on every image.
- **Color contrast** fixed: header and footer text changed from black on `#333333` (about 1.7:1) to white (12.6:1). Navigation links are 9.7:1 and body text 15.9:1.
- **Semantic HTML**: `<header>`, `<nav>`, `<main>`, `<section>` and `<footer>` instead of `<div>`; the navigation is a `<ul>` list.
- **Skip link** ("Skip to main content") as the first focusable element on each page.
- **Heading structure**: one `<h1>` per page followed by `<h2>` sections (the menu previously jumped from `<h1>` to `<h3>`).
- Removed the "Contact" link, which pointed to `#` and had no page behind it.

### 3. Styles
- All styles live in `styles.css`; the inline `<style>` block was removed.
- Removed deprecated and presentational attributes (`border="0"` on `<table>`, `type="text/css"`).
- CSS organized into numbered, commented sections and uses custom properties (variables) for colors, fonts and layout.

### 4. Images
- `srcset` and `sizes` serve 400, 800 or 1200px versions depending on screen width and pixel density.
- Images compressed (JPEG, quality 75–80, metadata removed). The chef photo was converted from PNG to JPEG.
- Total image weight on the home page went from about 1.9 MB to under 200 KB.
- `width`/`height` attributes prevent layout shift; `loading="lazy"` defers images below the fold.

### 5. User experience
- ARIA landmark roles (`banner`, `navigation`, `main`, `contentinfo`), `aria-label` on the navigation, `aria-current="page"` on the active link and `aria-labelledby` on each section.
- Visible `:focus-visible` indicators for links, buttons and form fields (yellow on dark backgrounds, blue on light ones).
- Tested keyboard-only navigation with Tab, Shift+Tab and Enter.

## Tools and resources
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
- [W3C HTML Validator](https://validator.w3.org/) and [CSS Validator](https://jigsaw.w3.org/css-validator/)
- Lighthouse (Chrome DevTools) and [WAVE](https://wave.webaim.org/)
- Python Pillow for resizing and compressing images
- [MDN — Responsive images](https://developer.mozilla.org/en-US/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images), [MDN — CSS Grid](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout), [CSS-Tricks — Flexbox guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)

## How to view the website
- Online: open https://lore-osorio.github.io/C2-restaurant-website-lore/
- Locally: clone the repository and open `index.html` in a browser:

```bash
git clone https://github.com/lore-osorio/C2-restaurant-website-lore.git
cd C2-restaurant-website-lore
```
