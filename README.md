# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Best Air Purifier landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Policy Pages](#adding-policy-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and brand name. To update:

1. **Brand Name:**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">BestAirPurifier</a>
```
Replace "BestAirPurifier" with your desired brand name.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Features</a>
```
- Update text between `>` and `</a>`
- Keep the `class` attributes to maintain styling
- Don't remove `transition-colors duration-200` as it controls hover animations

### Hero Section
Located at the top of the page with a large background image:

```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6">Best Air Purifier</h1>
<p class="text-xl md:text-2xl text-white mb-8">Find Best Air Purifier</p>
```
- `text-4xl` controls text size on mobile
- `md:text-6xl` controls text size on desktop
- Keep both to maintain responsive design

### Tailwind CSS Tips for Beginners
- Numbers in classes (like `text-4xl`) control size
- `md:` prefix means "apply on medium screens and up"
- `mb-6` means "margin bottom" (spacing)
- Don't remove responsive prefixes (`md:`, `lg:`)

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://stripe.com/buy">Buy Now</a>
```

2. Call-to-Action Links:
```html
<!-- Shop Now button in hero section -->
<a href="https://stripe.com/buy" class="inline-block bg-indigo-600...">Shop Now</a>
```

### Updating Links
1. Internal Links (sections on same page):
- Keep the `#` symbol
- Match the `id` of the target section
```html
<!-- Example: Linking to Features section -->
<a href="#features">Features</a>

<!-- Corresponding section -->
<section id="features" class="py-24 bg-white">
```

2. External Links:
- Replace `https://stripe.com/buy` with your actual purchase URL
- Always include `https://` for external links
```html
<!-- Example updating purchase link -->
<a href="https://your-store.com/product">Buy Now</a>
```

## Adding Policy Pages

### Footer Policy Links
Current placeholder structure:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Policies</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-200">Shipping Policy</a></li>
    </ul>
</div>
```

To link policy pages:
1. Create your policy pages (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section `id` matches the link `href`
- IDs are case-sensitive
- Remove any spaces in IDs

2. **Responsive Design Issues**
- Don't remove `md:` prefixed classes
- Keep both mobile and desktop size classes
- Test on different screen sizes

3. **Style Problems**
- Maintain the full class string when updating
- Don't remove Tailwind utility classes
- Keep hover states (`hover:`) for interactive elements

### Getting Help
If you encounter issues:
1. Check the Tailwind CSS documentation
2. Verify HTML syntax
3. Test links in different browsers
4. Use browser developer tools to inspect elements

Remember to always make a backup before making changes to the code.

---
This guide specifically references the provided landing page structure. For additional customization needs or technical support, consult the Tailwind CSS documentation or seek professional web development assistance.