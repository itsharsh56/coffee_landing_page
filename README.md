# Coffe Landing Page

A responsive static landing page for a coffee shop or cafe brand. The page presents a glass-style hero layout with navigation, a large marketing headline, short descriptive copy, and a coffee product image.

> Note: The project name and visible logo text currently use `Coffe`. If this is meant to be standard English, rename it to `Coffee` in `index.html`, the folder name, and this README.

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [File Details](#file-details)
- [Assets](#assets)
- [How to Run](#how-to-run)
- [How It Works](#how-it-works)
- [Responsive Design](#responsive-design)
- [Customization Guide](#customization-guide)
- [Deployment](#deployment)
- [Browser Support](#browser-support)
- [Accessibility Notes](#accessibility-notes)
- [Known Limitations](#known-limitations)
- [Future Improvements](#future-improvements)
- [Troubleshooting](#troubleshooting)

## Project Overview

This project is a front-end-only landing page built with plain HTML and CSS. It does not use JavaScript, a package manager, a build tool, or a backend server.

The design uses a warm coffee-inspired color palette, a blurred glass container, large typography, simple navigation links, hover effects, and responsive layout changes for tablets and phones.

## Features

- Single-page coffee landing page.
- Responsive navigation and hero content.
- Glassmorphism-style content container.
- Coffee-themed background gradient.
- Decorative circular accent created with CSS `clip-path`.
- Google Fonts integration using the Poppins font family.
- Hover animation for the text logo.
- Hover underline animation for navigation links.
- Responsive image sizing across desktop, tablet, and mobile screens.
- No JavaScript required.
- No installation required.

## Tech Stack

- HTML5
- CSS3
- Google Fonts
- Static image assets in PNG format

## Project Structure

```text
coffe landing page/
|-- index.html
|-- styles.css
|-- img.png
|-- logo.png
`-- README.md
```

## File Details

### `index.html`

The main HTML file. It defines the page structure:

- HTML document metadata.
- Link to `styles.css`.
- Main wrapper using `.container`.
- Navigation section with:
  - Text logo: `Coffe`.
  - Navigation links: `Home`, `About`, and `Contact`.
- Hero content section with:
  - Main headline: `Specialty Coffee and Delicious Treats`.
  - Introductory paragraph.
  - Product image loaded from `img.png`.

Current page title:

```html
<title>Document</title>
```

Recommended improvement:

```html
<title>Coffe Landing Page</title>
```

### `styles.css`

The main stylesheet. It controls layout, typography, colors, hover effects, and responsive behavior.

Important CSS parts:

- Imports Poppins from Google Fonts.
- Defines the main accent color in `:root`.
- Applies global reset styles with `*`.
- Creates the dark coffee background on `body`.
- Adds the circular accent shape with `body::after`.
- Styles the main `.container` with blur, transparency, rounded corners, and shadow.
- Uses Flexbox for the navigation and hero layout.
- Uses media queries for tablet and mobile responsiveness.

Main CSS variable:

```css
:root {
    --coffe: #C8835A;
}
```

## Assets

| File | Type | Dimensions | Size | Current Usage |
| --- | --- | ---: | ---: | --- |
| `img.png` | PNG image | 480 x 746 | 185,576 bytes | Used in the hero image section |
| `logo.png` | PNG image | 700 x 540 | 14,379 bytes | Present in the project but not currently used |

The page currently uses a text-based logo through this HTML:

```html
<a href="#" id="logo">Coffe</a>
```

If you want to use `logo.png`, replace the text logo with an image element and update the CSS accordingly.

## How to Run

Because this is a static HTML and CSS project, no installation is needed.

1. Open the project folder.
2. Double-click `index.html`.
3. The page will open in your default browser.

Alternative option:

1. Open the folder in VS Code.
2. Install the Live Server extension.
3. Right-click `index.html`.
4. Select `Open with Live Server`.

## How It Works

The project is divided into two main sections:

### Navigation

The navigation is built with a `nav` element. It contains the text logo and three placeholder links.

```html
<nav>
    <a href="#" id="logo">Coffe</a>
    <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
    </ul>
</nav>
```

The navigation links currently use `#`, so they do not navigate to real sections yet.

### Hero Content

The hero section uses `.content`, with text on one side and an image on the other.

```html
<div class="content">
    <div class="text">
        <h1>Specialty Coffee <br> and Delicious Treats</h1>
        <p>...</p>
    </div>
    <div class="image">
        <img src="img.png" alt="coffee and pastries">
    </div>
</div>
```

On smaller screens, the layout changes from side-by-side to stacked.

## Responsive Design

The stylesheet includes two responsive breakpoints.

### Screens up to 850px

At `max-width: 850px`:

- Navigation and content widths become smaller.
- Logo font size is reduced.
- Navigation gap is reduced.
- Hero layout changes to `column-reverse`.
- Content is centered.
- Heading becomes `40px`.
- Paragraph becomes `16px`.
- Hero image width becomes `150px`.

### Screens up to 550px

At `max-width: 550px`:

- Navigation gap is reduced again.
- Navigation link size becomes `14px`.
- Heading becomes `30px`.
- Paragraph becomes `14px`.
- Hero image width becomes `100px`.

## Customization Guide

### Change the Main Accent Color

Edit this variable in `styles.css`:

```css
:root {
    --coffe: #C8835A;
}
```

### Change the Background

Edit the `body` background gradient:

```css
body {
    background: linear-gradient(to left, #2b1301, #491f04);
}
```

### Change the Hero Text

Edit the heading and paragraph inside `.content .text` in `index.html`.

### Change the Hero Image

Replace `img.png` with another image, or update this line:

```html
<img src="img.png" alt="coffee and pastries">
```

Use a meaningful `alt` value that describes the new image.

### Add Real Navigation Sections

Create matching sections in `index.html` and update the links:

```html
<a href="#about">About</a>
<a href="#contact">Contact</a>
```

Then add corresponding sections:

```html
<section id="about"></section>
<section id="contact"></section>
```

## Deployment

This project can be deployed on any static hosting platform.

Good options include:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- Firebase Hosting

No build command is required. The publish directory is the project root.

## Browser Support

The page uses modern CSS features, including:

- Flexbox
- CSS variables
- `backdrop-filter`
- `clip-path`
- media queries

Most modern browsers support these features. The glass blur effect from `backdrop-filter` may look different in older browsers.

## Accessibility Notes

Current accessibility-friendly details:

- The main image includes alt text.
- Navigation is wrapped in a semantic `nav` element.
- Text contrast is generally strong because the text is white on a dark background.

Recommended improvements:

- Replace the generic page title with a descriptive title.
- Add real navigation destinations instead of `#` placeholders.
- Consider adding a visible focus state for keyboard users.
- Use semantic sections if more page content is added.
- Check color contrast after any palette changes.

## Known Limitations

- The navigation links are placeholders and do not go anywhere yet.
- `logo.png` exists but is not used in the current page.
- The HTML title is still `Document`.
- The visible brand name is spelled `Coffe`.
- There is no JavaScript interactivity.
- There is no contact form, menu section, about section, or footer.
- The layout is designed as a landing-page hero, not a complete multi-section website.
- The Poppins font loads from Google Fonts, so the exact font depends on internet access.

## Future Improvements

- Correct the brand name to `Coffee` if needed.
- Add a real cafe logo image.
- Add a menu section for drinks and pastries.
- Add an about section.
- Add a contact section with address, phone number, and opening hours.
- Add a footer.
- Add real navigation anchors.
- Add better keyboard focus styles.
- Add SEO metadata.
- Add Open Graph metadata for social sharing.
- Add a favicon.
- Optimize images for faster loading.
- Add a screenshot preview to this README.

## Troubleshooting

### The font does not look like the preview

The project imports Poppins from Google Fonts. If you are offline or Google Fonts is blocked, the browser will fall back to a generic sans-serif font.

### The blur effect does not appear

The glass effect uses `backdrop-filter`. Some older browsers may not fully support it.

### The page does not navigate when clicking Home, About, or Contact

Those links currently use `#`. Add real page sections and update the link targets to make them functional.

### The image does not load

Make sure `img.png` is in the same folder as `index.html`, and confirm that the file name matches exactly.

## Maintenance Notes

- Keep `index.html`, `styles.css`, and images in the same folder unless you update the file paths.
- If you rename image files, update the matching `src` values in `index.html`.
- If you add new CSS files, link them in the `<head>` of `index.html`.
- If you add JavaScript later, place the script tag before the closing `</body>` tag or use `defer` in the `<head>`.

