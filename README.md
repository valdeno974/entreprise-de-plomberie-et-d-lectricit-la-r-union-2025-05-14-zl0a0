# Landing Page Maintenance Guide

This guide will help you maintain and customize the PEReunion landing page. Follow these instructions carefully to make updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu:

```html
<div class="text-xl font-bold text-blue-600">PEReunion</div>
```
To update the company name:
1. Locate this div in the header section
2. Replace "PEReunion" with your desired text
3. Adjust text size using Tailwind classes:
   - `text-xl` (current size)
   - `text-2xl` (larger)
   - `text-lg` (smaller)

### Hero Section
The main headline and subtitle are located in:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Entreprise de plomberie et d'électricité à La Réunion
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    Vos travaux de plomberie et d'électricité à la Réunion
</p>
```

To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Replace the text between the `<p>` tags for the subtitle
3. Keep the responsive classes (`md:` and `lg:` prefixes) to maintain mobile compatibility

### Service Cards
Each service card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300 border border-gray-100">
    <h3 class="text-xl font-semibold mb-4 text-gray-900">Service Title</h3>
    <p class="text-gray-600">Service Description</p>
</div>
```

To update:
1. Locate the service cards in the `#services` section
2. Replace "Service Title" with your service name
3. Replace "Service Description" with your service details
4. Maintain the existing classes for consistent styling

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Services</a>
    <a href="#avantages" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Avantages</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. The `href="#services"` format links to sections within the page
2. To link to external pages, replace with full URLs:
   ```html
   <a href="https://example.com/services">Services</a>
   ```
3. For internal pages, use relative paths:
   ```html
   <a href="./services.html">Services</a>
   ```

### Footer Links
Current footer links need updating:

```html
<ul class="space-y-2">
    <li><a href="#" class="hover:text-white transition-colors duration-300">Dépannage</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Rénovation</a></li>
    <li><a href="#" class="hover:text-white transition-colors duration-300">Installation</a></li>
</ul>
```

Replace `href="#"` with proper URLs or page paths.

## Linking Privacy and Terms Pages

### Adding Privacy and Terms Links
In the footer's legal section:

```html
<div>
    <h3 class="text-white font-semibold text-lg mb-4">Légal</h3>
    <ul class="space-y-2">
        <li><a href="./privacy.html" class="hover:text-white transition-colors duration-300">Mentions légales</a></li>
        <li><a href="./terms.html" class="hover:text-white transition-colors duration-300">Politique de confidentialité</a></li>
    </ul>
</div>
```

To implement:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the `href` attributes to point to these files
3. Maintain the existing classes for consistent styling

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs and hrefs
   - Verify file paths for internal pages

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header
   - Test on multiple screen sizes

3. **Style Inconsistencies**
   - Copy existing Tailwind classes when adding new elements
   - Maintain the color scheme using existing color classes
   - Keep spacing consistent using existing margin/padding classes

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check that all HTML tags are properly closed
- Validate your HTML using [W3C Validator](https://validator.w3.org/)

Remember to test all changes across different devices and browsers before deploying to production.