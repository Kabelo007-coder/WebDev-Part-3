# Kay's Clothing Co. (My Changes and Additions)
Kabelo Mogale ST10457105


## What I Changed & Added

### 1. Fixed Critical Bug - White Dot on Desktop
- **Problem:** There was a white floating button was showing on top-right on desktop, covering content. It was meant to be a mobile-only menu.
- **Fix:** 
    - Added `display: none;` to desktop CSS for `#mobileMenuToggle`
    - Added `@media (min-width: 769px)` rule to hide `#navLinks.active` on desktop
    - Made toggle button yellow (#fbbf24) and visible only on mobile (max-width: 768px)

### 2. Fixed Mobile Navigation
- **Problem:** Hamburger menu was not opening properly, navLinks class conflicted with desktop styles.
- **Fix:** 
    - Created proper `.nav-links` flex layout for desktop
    - Mobile: nav becomes dropdown with `position: absolute` and background #0f2442
    - Added JavaScript toggle in kayscript.js with aria-expanded for accessibility

### 3. Fixed Duplicate Enquiry Forms
- **Problem:** Two enquiry forms were showing on enquiries.html
- **Fix:** Removed duplicate form container, kept single form with proper id="enquiryForm"

### 4. Added Brooklyn Maps Feature
- **Added:** Two maps - Mamelodi (main branch) and Brooklyn (new branch)
- **Function:** Toggle button switches between maps using JavaScript `switchMap()` function
- **Files:** `contact.html` - added map containers and toggle logic

### 5. Gallery Lightbox
- **Added:** Click image to open lightbox modal
- **Fix:** Added `data-src` attributes and `loading="lazy"` for performance
- **Accessibility:** Added aria-labels and keyboard ESC to close lightbox

### 6. General Improvements
- Added responsive meta viewport (already present but verified)
- Optimized images with width/height to prevent layout shift
- Added form validation in kayscript.js
- Made header sticky and improved footer layout

## Technologies Used
- HTML5
- CSS3 (Flexbox, Grid, Media Queries)
- Vanilla JavaScript
- Netlify for deployment
- Git & GitHub for version control

## How to Run Locally
1. Clone repo
2. Open index.html in browser

## Challenges Faced
- The white dot was caused by mobile menu toggle showing on desktop due to missing media query.
- Solved by separating desktop and mobile CSS.

## References
- MDN Web Docs for CSS Grid and Flexbox
- Netlify Docs for deployment
