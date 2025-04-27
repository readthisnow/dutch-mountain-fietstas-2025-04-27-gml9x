# Dutch Mountain Landing Page - Maintenance Guide

This guide will help you maintain and customize the Dutch Mountain landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Located in the header section -->
<a href="#" class="text-2xl font-bold text-gray-900">Dutch Mountain</a>
```
Simply replace "Dutch Mountain" with your desired text.

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
</div>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
The main banner section contains:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Dutch Mountain Fietstas
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Tijdelijk 10% Korting | Nog maar enkele stuks beschikbaar!
</p>
```
- Change the heading by modifying text within the `<h1>` tags
- Update the promotional text within the `<p>` tags

### Tailwind CSS Tips for Beginners
Common classes explained:
- `text-4xl`: Sets text size (ranges from text-xs to text-9xl)
- `md:text-5xl`: Applies style at medium screen sizes
- `font-bold`: Makes text bold
- `mb-6`: Adds margin bottom (spacing)
- `text-gray-900`: Sets text color

To modify styles:
1. Find the element you want to change
2. Locate its class attribute
3. Add or modify Tailwind classes separated by spaces
4. Test on different screen sizes using browser dev tools

## Managing Links

### Current Link Inventory
1. Navigation Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
```

2. Call-to-Action Links:
```html
<a href="https://amzn.to/3EFW4lo" class="bg-blue-600 text-white">
    Koop Nu
</a>
```

3. Footer Links:
```html
<a href="#">Privacy Policy</a>
<a href="#">Terms & Conditions</a>
<a href="#">Facebook</a>
<a href="#">Instagram</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. For internal links (same page):
   - Use `#section-id` format
   - Ensure the referenced section has matching ID
4. For external links:
   - Use complete URLs starting with `https://`
   - Test links after updating

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace placeholder links with:
```html
<!-- In the footer section -->
<ul class="space-y-2">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms & Conditions</a></li>
</ul>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match exactly:
```html
<!-- Link -->
<a href="#features">Features</a>

<!-- Matching section -->
<section id="features">
```

2. **Responsive Design Issues**
- Verify screen-specific classes:
```html
class="text-4xl md:text-5xl lg:text-6xl"
```
- Test at different screen sizes
- Common breakpoints:
  - `md:` (768px)
  - `lg:` (1024px)

3. **Style Changes Not Applying**
- Check for typos in Tailwind classes
- Ensure classes are space-separated
- Verify the Tailwind CDN is loading properly:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Test all changes across different devices and browsers

Remember to always backup your files before making significant changes!