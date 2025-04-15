# Texas Web Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-blue-600">Texas Web</a>
```
Simply replace "Texas Web" with your desired text.

### Hero Section
Located at the top of the page with the main heading and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">Custom Websites For Your Business</p>
```

Key Tailwind classes explained:
- `text-4xl`: Large text on mobile
- `md:text-5xl`: Larger text on medium screens
- `lg:text-6xl`: Largest text on large screens
- `mb-6`: Margin bottom spacing
- `leading-tight`: Reduced line height

### Features Section
To modify feature cards:

1. Locate the feature card structure:
```html
<div class="bg-white rounded-2xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-magic text-2xl text-blue-600"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Easy to Use</h3>
    <p class="text-gray-600 leading-relaxed">Intuitive interface and user-friendly design...</p>
</div>
```

To change icons:
1. Find the `<i>` tag
2. Replace the Font Awesome class (e.g., `fa-magic`) with a different icon from [Font Awesome](https://fontawesome.com/icons)

## Managing Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-700 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute
2. For internal links (same page sections), use `#section-id`
3. For external links, use the full URL: `https://example.com`

### Call-to-Action Buttons
Current CTA links point to "https://sigmaseo.io". To update:

```html
<!-- Find these buttons -->
<a href="https://sigmaseo.io" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>
```

Replace the `href` value with your desired URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the footer section and update the placeholder links:

```html
<!-- Before -->
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>

<!-- After -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Example: `href="#features"` needs a matching `id="features"` in the target section

2. **Responsive Design Issues**
   - Check that you've maintained the responsive classes:
     - `md:` prefix for medium screens
     - `lg:` prefix for large screens
   - Don't remove `container` and `mx-auto` classes as they maintain proper spacing

3. **Icon Not Showing**
   - Verify the Font Awesome CDN link is present in the head section
   - Check that icon class names are correct
   - Example: `fas fa-magic` should include both the style prefix (`fas`) and icon name (`fa-magic`)

### Getting Help
If you encounter issues:
1. Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
2. Verify all CDN links are working
3. Use browser developer tools (F12) to inspect elements
4. Ensure all HTML tags are properly closed

Remember to test all changes across different screen sizes using browser developer tools before deploying to production.