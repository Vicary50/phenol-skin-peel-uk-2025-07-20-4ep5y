# Phenol Skin Peel Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Phenol Skin Peel landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-gray-800">PhenolPeel</a>
```
- Replace "PhenolPeel" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
- Update text between `>` and `</a>`
- Keep the same class structure to maintain hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-gray-900 tracking-tight mb-8">
    Phenol Skin Peel UK
</h1>
<p class="text-xl sm:text-2xl text-gray-600 leading-relaxed mb-12">
    Experience the gold standard in facial skin peel
</p>
```
- Update text while maintaining the existing classes
- `sm:` and `lg:` prefixes control responsive behavior
- `mb-8` controls bottom margin (8 = 2rem)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition duration-300">
    <h3 class="text-xl font-semibold mb-4">Smooth Wrinkles</h3>
    <p class="text-gray-600">Advanced treatment to reduce...</p>
</div>
```
- Update heading and paragraph text
- Maintain the class structure for consistent styling
- `p-8` controls padding (8 = 2rem)

## Managing Links

### Navigation Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://phenolskinpeel.co.uk">Book Now</a>
```

To update:
1. Internal links (starting with #):
   - Match the `id` of the section you're linking to
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace `https://phenolskinpeel.co.uk` with your booking URL
   - Always include `https://` for external links

### Footer Links
Located at the bottom of the page:
```html
<div>
    <h3 class="text-xl font-bold text-white mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <li><a href="#features">Features</a></li>
        <!-- More links -->
    </ul>
</div>
```

To update:
1. Replace `href` values
2. Maintain the class structure
3. Test all links after updating

## Adding Privacy and Terms Pages

### Step 1: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h3 class="text-xl font-bold text-white mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

Replace the `#` with proper paths:
```html
<li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 2: Create Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in `href` attributes
   - Verify file paths are correct
   - Ensure all referenced IDs exist

2. **Styling Problems**
   - Don't remove `class` attributes
   - Keep responsive prefixes (`sm:`, `md:`, `lg:`)
   - Maintain spacing classes (`mb-8`, `p-8`, etc.)

3. **Mobile Menu Issues**
   - Keep the Alpine.js script tag in the header
   - Don't modify `x-data` attributes
   - Maintain the mobile menu button structure

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Alpine.js is loading properly
- Test on multiple devices and browsers

Remember to always backup your files before making changes and test thoroughly after updates.