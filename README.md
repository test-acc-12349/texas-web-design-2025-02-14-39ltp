# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<div class="text-2xl font-bold text-blue-600">
    Texas Web Design  <!-- Change company name here -->
</div>
```

#### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Best Websites In Texas  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Professional web design solutions...  <!-- Update subheadline here -->
</p>
```

### Tailwind CSS Classes Explained

#### Common Classes Used:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `bg-[color]`: Sets background color (e.g., `bg-blue-600`)
- `p-[size]`: Sets padding (e.g., `p-8`)
- `m-[size]`: Sets margin (e.g., `mb-4`)

#### Responsive Design Classes:
```html
<!-- Example of responsive text -->
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
- `text-4xl`: Default size on mobile
- `md:text-5xl`: Size on medium screens
- `lg:text-6xl`: Size on large screens

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace `#section-name` with:
   - For same-page links: Keep `#section-name`
   - For external links: Use full URL (e.g., `https://example.com`)
   - For internal pages: Use relative path (e.g., `about.html`)

### Social Media Links
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition duration-300">
        <i class="fab fa-facebook text-2xl"></i>
    </a>
    <!-- Replace # with actual social media URLs -->
</div>
```

## Linking Privacy and Terms Pages

### Current Footer Structure
```html
<div>
    <h3 class="text-xl font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages:
1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the links in footer:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

3. Maintain consistent styling by copying these classes:
   - `hover:text-white`
   - `transition duration-300`

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Ensure file names are correct
   - Verify file locations in project folder

2. **Responsive Design Issues**
   - Check for proper responsive classes (`md:`, `lg:`)
   - Test on different screen sizes
   - Verify mobile menu functionality

3. **Style Inconsistencies**
   - Compare Tailwind classes with existing elements
   - Maintain color scheme (`blue-600`, `gray-900`, etc.)
   - Keep consistent spacing (`p-8`, `mb-4`, etc.)

### Need Help?
- Check [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always backup your files before making changes, and test all modifications across different devices and browsers.