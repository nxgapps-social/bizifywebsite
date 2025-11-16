# CLAUDE.md - Bizify Technology Website

## Project Overview

**Bizify Technology** is a digital agency website showcasing services including digital marketing, software development, market leads, and data analytics. This is a static, single-page application (SPA) built with vanilla HTML, CSS, and JavaScript.

### Project Type
- Static marketing website
- Single-page application
- No build process or bundler required
- Production-ready static files

### Tech Stack
- **HTML5**: Semantic markup
- **CSS3**: Custom properties (CSS variables), flexbox, grid
- **JavaScript (ES6)**: Vanilla JS for interactivity
- **External Dependencies**:
  - Google Fonts: Poppins & Cuprum
  - Ionicons v5.5.2: Icon library

---

## Repository Structure

```
bizifywebsite/
├── assets/
│   ├── css/
│   │   └── style.css           # Main stylesheet (1135 lines)
│   ├── js/
│   │   └── script.js           # Main JavaScript (76 lines)
│   └── images/
│       ├── about-banner.png
│       ├── bizify.png
│       ├── hero-banner.png
│       ├── hero-pattern.svg
│       ├── service-1.png
│       ├── service-2.png
│       ├── service-3.png
│       └── service-4.png
├── readme-images/
│   └── desktop.png
├── favicon.svg
├── favicon2.svg
├── index.html                   # Main HTML file (705 lines)
├── index.txt
├── README.md                    # Project documentation
└── style-guide.md              # Design system reference
```

---

## File Descriptions

### Core Files

#### `index.html` (Main Entry Point)
- **Location**: `/home/user/bizifywebsite/index.html`
- **Purpose**: Single-page website structure
- **Sections**:
  - **Header** (lines 42-96): Fixed navigation with mobile menu
  - **Hero** (lines 109-134): Welcome section with CTA
  - **About** (lines 144-191): Company introduction
  - **Services** (lines 201-327): Service offerings grid
  - **Features** (lines 337-437): Value propositions (6 cards)
  - **FAQ** (lines 447-530): Accordion-style FAQs
  - **Footer** (lines 543-685): Contact info, links, newsletter
- **Key Attributes**:
  - Uses data attributes for JavaScript hooks: `data-header`, `data-navbar`, `data-nav-toggler`, etc.
  - Semantic HTML5 elements
  - External form integration: Typeform (https://h5ugb3q8ncl.typeform.com/c/IyPDMk6F)

#### `assets/css/style.css`
- **Location**: `/home/user/bizifywebsite/assets/css/style.css:1`
- **Purpose**: Complete styling system
- **Structure**:
  - Custom Properties (lines 17-87): CSS variables for theming
  - Reset Styles (lines 97-158): Browser normalization
  - Reused Styles (lines 166-270): Common utilities
  - Component Styles (lines 276-804): Section-specific styles
  - Media Queries (lines 817-1135): Responsive breakpoints
- **Design System**:
  - Colors: Green accent (`--go-green: hsl(145, 63%, 42%)`), dark backgrounds
  - Typography: Cuprum (headings), Poppins (body)
  - Breakpoints: 575px, 768px, 992px, 1200px
  - Responsive approach: Mobile-first

#### `assets/js/script.js`
- **Location**: `/home/user/bizifywebsite/assets/js/script.js:1`
- **Purpose**: Interactive functionality
- **Features**:
  - **Utility**: `addEventOnElem` function (lines 9-17) for event delegation
  - **Mobile Navigation** (lines 25-34): Toggle navbar and overlay
  - **Auto-close Nav** (lines 42-49): Close on link click
  - **Sticky Header** (lines 57-64): Add 'active' class on scroll > 100px
  - **FAQ Accordion** (lines 72-76): Toggle FAQ answers
- **Code Style**: ES6 arrow functions, strict mode

#### `style-guide.md`
- **Location**: `/home/user/bizifywebsite/style-guide.md:1`
- **Purpose**: Design system reference for developers
- **Contents**:
  - Color palette with HSL values
  - Typography scale (12 font sizes)
  - Spacing system
  - Shadow definitions
  - Border radius values
  - Transition timing functions
  - External resource links

---

## Development Workflow

### Local Development

1. **No Build Required**: This is a static site - simply open `index.html` in a browser
2. **Live Server Recommended**: Use VS Code Live Server or similar for hot reload
3. **File Watching**: Not required (no compilation step)

### Testing Locally

```bash
# Option 1: Python SimpleHTTPServer
python3 -m http.server 8000

# Option 2: Node http-server (if installed)
npx http-server -p 8000

# Option 3: PHP built-in server
php -S localhost:8000
```

Then navigate to `http://localhost:8000`

### Making Changes

#### HTML Changes (`index.html`)
- **Sections are clearly commented**: Look for `<!-- - #SECTION_NAME -->`
- **Data attributes**: Maintain `data-*` attributes for JavaScript functionality
- **Contact Form**: External Typeform integration at `https://h5ugb3q8ncl.typeform.com/c/IyPDMk6F`
- **Phone Numbers**:
  - USA: +1-5133608501 (line 76)
  - India: +91-9178658918 (line 80)
- **Email**: support@bizifytech.com (line 637)

#### CSS Changes (`assets/css/style.css`)
- **Use CSS Variables**: All theme values in `:root` (lines 17-87)
- **Color Changes**: Modify `--go-green` for accent color changes
- **Responsive Design**: Mobile-first approach - base styles, then media queries
- **Component Pattern**: Each section has dedicated styles (HEADER, HERO, ABOUT, etc.)
- **Naming Convention**: BEM-like class names (`.section-title`, `.card-content`, etc.)

#### JavaScript Changes (`assets/js/script.js`)
- **Minimal Dependencies**: Pure vanilla JavaScript
- **Event Delegation**: Use `addEventOnElem` utility for consistency
- **Class Toggling**: Primary interaction method
- **Selectors**: Query by data attributes (`[data-navbar]`, `[data-header]`, etc.)

### Image Updates

**Location**: `/home/user/bizifywebsite/assets/images/`

**Current Images**:
- `hero-banner.png` (650x650px): Main hero image
- `about-banner.png` (802x654px): About section image
- `service-1.png` to `service-4.png` (140x140px): Service icons
- `hero-pattern.svg`: Background pattern for hero
- `bizify.png`: Logo/branding

**Image Optimization**:
- Compress images before adding
- Maintain aspect ratios specified in HTML
- Use WebP format for better performance (update HTML accordingly)

---

## Key Conventions for AI Assistants

### Code Style Guidelines

#### HTML
- Use semantic HTML5 elements (`<header>`, `<section>`, `<article>`, `<footer>`)
- Maintain data attributes for JavaScript hooks
- Keep accessibility attributes (`aria-label`, `aria-hidden`)
- Comments use format: `<!-- - #SECTION_NAME -->`
- Indentation: 2 spaces

#### CSS
- **Organization**: Follow existing section order
- **Selectors**: Use class selectors, avoid IDs
- **Variables**: Always use CSS custom properties from `:root`
- **Responsive**: Add mobile styles first, then media query overrides
- **Comments**: Section headers use format `/*-----------------------------------*\`
- **Property Order**: Logical grouping (positioning → box model → typography → visual)
- Indentation: 2 spaces

#### JavaScript
- **Mode**: Use `'use strict';` at file top
- **Style**: ES6 syntax (arrow functions, const/let)
- **Event Handling**: Use `addEventOnElem` utility function
- **Selectors**: Query by data attributes for JS-related elements
- **Naming**: camelCase for variables/functions
- Indentation: 2 spaces

### Common Tasks

#### Adding a New Section

1. **HTML** (`index.html`):
   ```html
   <!-- - #NEW_SECTION -->
   <section class="section new-section" id="new-section" aria-label="new section">
     <div class="container">
       <!-- Content here -->
     </div>
   </section>
   ```

2. **CSS** (`style.css`):
   ```css
   /*-----------------------------------*\
     #NEW_SECTION
   \*-----------------------------------*/

   .new-section {
     /* Styles here */
   }
   ```

3. **Navigation** (if needed):
   - Add link to navbar-list (around line 57-83 in index.html)
   - Ensure `data-nav-link` attribute is present

#### Updating Colors

**Primary Accent Color**:
```css
/* In style.css line 33 */
--go-green: hsl(145, 63%, 42%);  /* Change this */
```

**Background Colors**:
```css
--rich-black-fogra-29-1: hsl(215, 31%, 14%);  /* Headings */
--rich-black-fogra-29-2: hsl(230, 14%, 8%);   /* Footer */
--mint-cream: hsl(160, 100%, 98%);            /* Hero background */
```

#### Adding Interactive Elements

**Pattern to Follow**:
1. Add data attribute in HTML: `data-custom-action`
2. Query in JavaScript:
   ```javascript
   const customElements = document.querySelectorAll("[data-custom-action]");
   const handleCustom = function() { /* logic */ }
   addEventOnElem(customElements, "click", handleCustom);
   ```

#### Updating Contact Information

**Locations to Update**:
- Header navbar: lines 76, 80 (index.html)
- Footer contact section: lines 620-638 (index.html)
- Newsletter form: line 556-562 (index.html)

---

## Git Workflow

### Branch Strategy
- **Development Branch**: `claude/claude-md-mi1vck1i28jyea09-01FJ21jNdiXdgm8xXXeDNyY6`
- **Naming Pattern**: Branches must start with `claude/` and end with session ID
- **Main Branch**: Not specified (likely `main` or `master`)

### Commit Messages
Follow conventional commit format:
```
type: brief description

- Detailed point 1
- Detailed point 2
```

**Types**:
- `feat`: New feature
- `fix`: Bug fix
- `style`: CSS/design changes
- `docs`: Documentation updates
- `refactor`: Code restructuring
- `perf`: Performance improvements

### Push Strategy
```bash
git push -u origin claude/claude-md-mi1vck1i28jyea09-01FJ21jNdiXdgm8xXXeDNyY6
```

**Important**:
- Always push to the designated branch
- Retry up to 4 times with exponential backoff on network errors (2s, 4s, 8s, 16s)
- Branch name format must match or push will fail with 403

---

## External Dependencies & APIs

### Google Fonts
**Integration**: `<link>` in `<head>` (index.html lines 23-27)
```html
<link href="https://fonts.googleapis.com/css2?family=Cuprum:wght@500;600;700&family=Poppins:wght@400;500;600&display=swap" rel="stylesheet">
```

### Ionicons
**Integration**: Scripts before `</body>` (index.html lines 699-700)
```html
<script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
<script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>
```

**Usage in HTML**:
```html
<ion-icon name="menu-outline" aria-hidden="true"></ion-icon>
```

### Typeform Integration
**Contact Form**: External form at `https://h5ugb3q8ncl.typeform.com/c/IyPDMk6F`
- Used in: Header CTA, About section, Services CTA, FAQ section
- Alternative: Could be replaced with native HTML form + backend

---

## Performance Considerations

### Current Setup
- **No bundler**: All assets loaded individually
- **No minification**: Files are uncompressed
- **No lazy loading**: All images load immediately (except `loading="lazy"` on some)
- **External CDNs**: Fonts and icons from CDN

### Optimization Opportunities

1. **Image Optimization**:
   - Convert PNG to WebP
   - Add srcset for responsive images
   - Implement lazy loading on below-fold images

2. **CSS Optimization**:
   - Remove unused styles
   - Minify in production
   - Critical CSS inline in `<head>`

3. **JavaScript Optimization**:
   - Already minimal (76 lines)
   - Could add defer/async to script tags

4. **Caching Strategy**:
   - Add cache headers for assets
   - Version assets (style.css?v=1.0)

---

## Browser Support

### Target Browsers
Based on CSS features used:
- Chrome/Edge: Last 2 versions
- Firefox: Last 2 versions
- Safari: Last 2 versions
- Mobile Safari: iOS 12+
- Chrome Android: Last 2 versions

### Critical Features Used
- CSS Grid & Flexbox: IE11+ (with autoprefixer)
- CSS Custom Properties: No IE11 support
- ES6 JavaScript: No IE11 support
- Ionicons Web Components: Modern browsers only

**Recommendation**: Add transpilation/polyfills for IE11 support if needed

---

## Accessibility

### Current Accessibility Features
- Semantic HTML elements
- `aria-label` attributes on sections
- `aria-hidden` on decorative icons
- Keyboard navigation support (via native elements)
- Focus styles (`:focus-visible`)

### Improvements Needed
- Add skip-to-content link
- Test with screen readers
- Ensure color contrast ratios (WCAG AA)
- Add alt text to all images
- Ensure form labels are properly associated

---

## Testing Checklist

### Before Committing Changes

- [ ] Test on mobile viewport (< 575px)
- [ ] Test on tablet viewport (768px)
- [ ] Test on desktop viewport (1200px+)
- [ ] Verify mobile menu toggle works
- [ ] Verify FAQ accordion toggles work
- [ ] Check sticky header activates on scroll
- [ ] Validate HTML (https://validator.w3.org/)
- [ ] Check console for JavaScript errors
- [ ] Test all external links (Typeform, phone, email)
- [ ] Verify form submission (newsletter)

### Cross-Browser Testing
- [ ] Chrome/Edge
- [ ] Firefox
- [ ] Safari (if on macOS)
- [ ] Mobile Safari (if available)
- [ ] Chrome Android (if available)

---

## Common Issues & Solutions

### Issue: Mobile menu not closing on link click
**Solution**: Ensure `data-nav-link` attribute is present on navbar links (index.html:60-82)

### Issue: Header not becoming sticky
**Solution**: Check `data-header` attribute exists on header (index.html:42) and scroll event is firing (script.js:57-64)

### Issue: FAQ accordion not expanding
**Solution**: Verify `data-accordion-action` attribute on FAQ buttons (index.html:461) and JavaScript is loaded (script.js:72-76)

### Issue: Styles not applying
**Solution**:
1. Check CSS file is linked correctly (index.html:18)
2. Clear browser cache
3. Inspect element to see if styles are being overridden
4. Check media query breakpoints

### Issue: Icons not displaying
**Solution**:
1. Ensure Ionicons scripts are loaded (index.html:699-700)
2. Check icon names are valid (https://ionic.io/ionicons/v5)
3. Verify internet connection (icons load from CDN)

---

## Deployment

### Static Hosting Options
- **GitHub Pages**: Push to `gh-pages` branch
- **Netlify**: Connect repo, auto-deploy on push
- **Vercel**: Same as Netlify
- **AWS S3 + CloudFront**: Manual upload or CI/CD
- **Traditional Web Hosting**: FTP upload all files

### Deployment Checklist
- [ ] Update contact email/phone numbers
- [ ] Replace Typeform URL with production form
- [ ] Optimize images (WebP conversion, compression)
- [ ] Minify CSS and JavaScript
- [ ] Add meta tags for SEO
- [ ] Test all links
- [ ] Set up analytics (Google Analytics, etc.)
- [ ] Configure custom domain (if applicable)
- [ ] Set up SSL certificate
- [ ] Create sitemap.xml
- [ ] Create robots.txt

---

## Future Enhancements

### Suggested Improvements
1. **Build Process**: Add Webpack/Vite for bundling and optimization
2. **CSS Preprocessor**: Consider Sass/SCSS for better organization
3. **Form Handling**: Replace Typeform with native form + backend API
4. **Animation Library**: Add AOS (Animate On Scroll) or GSAP
5. **Blog Section**: Add blog/news section for content marketing
6. **Portfolio Section**: Showcase case studies and past work
7. **Testimonials**: Add client testimonials/reviews
8. **Multi-language**: Add i18n support for international clients
9. **Dark Mode**: Implement dark theme toggle
10. **Performance Monitoring**: Add Core Web Vitals tracking

---

## Contact & Support

### Project Information
- **Company**: Bizify Technology Pvt Ltd
- **Copyright**: © 2023 Bizify Technology Pvt Ltd
- **Email**: support@bizifytech.com
- **Phone (USA)**: +1-5133608501
- **Phone (India)**: +91-9178658918

### Physical Addresses
- **Office 1**: PLOT-HIG-32, 2ND FLOOR JAYADEV VIHAR, BHUBANESWAR ODISHA
- **Office 2**: D 168 Metro Satellite City, Phase 1, Puri Canal Road, Hanspal Bhubaneswar, 752101

---

## License

This project is **free to use** and does not contain any license (as per README.md:54).

**Note**: The README.md mentions "codewithsadee/hoolix" which suggests this may be based on a template. Consider adding proper attribution if required.

---

## Additional Resources

### Documentation Files
- **README.md**: Project overview and setup instructions
- **style-guide.md**: Complete design system reference
- **index.txt**: Unknown purpose (check if needed)

### Learning Resources
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [Ionicons Documentation](https://ionic.io/ionicons)
- [Google Fonts](https://fonts.google.com/)

---

**Last Updated**: 2025-11-16
**Document Version**: 1.0
**Maintained By**: Claude AI Assistant
