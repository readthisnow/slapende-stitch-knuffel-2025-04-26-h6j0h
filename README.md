# Landing Page Maintenance Guide

This guide will help you maintain and customize the Stitch Plush Toy landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To modify:

1. **Logo Text**:
```html
<div class="text-2xl font-bold text-blue-600">Stitch</div>
```
- Replace "Stitch" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)
- Change color using `text-blue-600` (options: text-red-600, text-green-600, etc.)

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-800 mb-6">
    Slapende Stitch Knuffel
</h1>
```
- Update the heading text between the tags
- The classes ensure responsive sizing:
  - `text-4xl`: Mobile size
  - `md:text-5xl`: Tablet size
  - `lg:text-6xl`: Desktop size

### Features Section
To modify feature cards:
```html
<div class="bg-blue-50 p-8 rounded-2xl hover:shadow-xl">
    <i class="fas fa-heart text-3xl text-blue-600 mb-4"></i>
    <h3 class="text-xl font-semibold mb-4">Super Zacht Materiaal</h3>
    <p class="text-gray-600">Perfect om mee te knuffelen en te slapen</p>
</div>
```
- Change icons by updating `fa-heart` to other FontAwesome icons
- Modify background color using `bg-blue-50` (options: bg-red-50, bg-green-50, etc.)
- Update text content between `<h3>` and `<p>` tags

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600">FAQ</a>
</div>
```
To update:
1. Locate the `href` attribute
2. For internal links (same page):
   - Use `#section-id` format
   - Ensure the target section has matching ID
3. For external links:
   - Replace with full URL (e.g., `https://example.com`)

### Call-to-Action Buttons
```html
<a href="https://amzn.to/4iwURuA" class="bg-blue-600 text-white px-6 py-2 rounded-full">
    Koop Nu
</a>
```
- Update the `href` with your product link
- Modify button text between the tags
- Change colors using:
  - `bg-blue-600`: Background color
  - `text-white`: Text color

## Adding Privacy and Terms Pages

### Footer Links Setup
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```

To link to policy pages:
1. Create new HTML files:
   ```
   privacy.html
   terms.html
   ```
2. Update the href attributes:
   ```html
   <a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a>
   <a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a>
   ```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match href attributes
   - Example: `href="#features"` needs `id="features"` on target section

2. **Responsive Design Issues**
   - Verify responsive classes are properly set:
     ```html
     class="text-4xl md:text-5xl lg:text-6xl"
     ```
   - Test on different screen sizes using browser dev tools

3. **Icon Not Showing**
   - Ensure FontAwesome is properly linked in header
   - Verify icon class names (e.g., `fa-heart`, `fa-star`)

### Tips for Testing Changes

1. Always preview changes in multiple browsers
2. Test responsive design at different screen sizes
3. Verify all links work before publishing
4. Check for consistent styling across sections

Remember to back up your files before making significant changes, and test thoroughly in a development environment before pushing to production.

Need additional help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).