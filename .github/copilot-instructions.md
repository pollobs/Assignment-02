# TechWave Project - AI Coding Instructions

## Project Overview
TechWave is a static podcast landing page built with vanilla HTML/CSS. The project uses external CDN resources (Font Awesome 7.0.1, Google Fonts "Inter") and maintains a clean asset-based structure. No build tools, frameworks, or JavaScript are present—this is a simple presentation site.

## Architecture & File Structure
- **index.html**: Single entry point containing the complete DOM structure with a header/navbar component
- **styles/styles.css**: Global styles with a reset section and component-specific rules
- **assets/**: 21 PNG image assets including branding (TechWave.png), social icons, and background elements (hero-bg.png, footer-bg.png)

## Critical Patterns & Conventions

### Styling Approach
1. **CSS Reset First**: styles.css begins with universal reset (`* { margin: 0; padding: 0; box-sizing: border-box; }`)
2. **Dark Theme**: Dark purple background (`rgba(26, 11, 46, 1)`) with borders using `rgba(65, 37, 103, 1)`
3. **Font System**: Uses "Inter" from Google Fonts as primary font family; utilities provide explicit font declarations via `.inter-font` class
4. **Padding Convention**: Spacing uses 24px units (e.g., `.header { padding: 24px 24px; }`)

### HTML Patterns
- Navigation built with `<ul>` + `<li>` + `<a>` semantic structure inside `.navbar` container
- Font Awesome icons injected via `<i class="fa-solid fa-[icon-name]"></i>` tags
- Images use relative `src="assets/[filename].png"` paths
- All pages wrapped in `.container` div for layout control

## Common Dev Tasks
- **Viewing Changes**: Open index.html directly in browser (no dev server required)
- **Adding Images**: Place PNG files in `assets/` directory, reference via `src="assets/filename.png"`
- **Updating Styles**: Edit `styles/styles.css` following the reset-then-components structure
- **Adding Navigation Links**: Update `<ul class="menu">` items in index.html

## External Dependencies
- **Font Awesome 7.0.1** (CDN with SRI hash)
- **Google Fonts** (Inter, preconnect enabled for performance)

## Special Considerations
- No JavaScript—all interactivity must be CSS-based
- No package.json or build step required
- Color system uses RGBA notation (preserve when extending)
- All href attributes are empty strings (`href=""`); update as routes are defined
