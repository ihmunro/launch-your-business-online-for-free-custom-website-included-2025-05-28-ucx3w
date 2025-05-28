# Landing Page Maintenance Guide

This guide will help you maintain and customize your FreeBizSite landing page. Follow these detailed instructions to make common updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your site name and navigation menu. To update:

1. Change the site name:
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    FreeBizSite  <!-- Replace this text -->
</a>
```

2. Modify navigation items:
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these text values as needed -->
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    <!-- Replace this headline -->
    Launch Your Business Online for Free — Custom Website Included
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    <!-- Replace this subheading -->
    Get a High-Converting Website for Your Business - 100% Free
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Sets font size (increases with md: and lg: prefixes)
- `font-bold`: Makes text bold
- `mb-8`: Adds margin bottom (spacing)
- `bg-gray-900`: Sets background color
- `text-gray-100`: Sets text color
- `hover:text-white`: Changes text color on hover

## Managing Links

### Navigation Menu Links
The page uses anchor links to scroll to sections. Update these in two places:

1. Desktop menu:
```html
<div class="hidden md:flex space-x-8">
    <!-- Update href attributes to match your section IDs -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

2. Mobile menu:
```html
<div x-show="isOpen" class="md:hidden mt-4 space-y-4">
    <!-- Update these to match desktop menu changes -->
    <a href="#features">Features</a>
    <!-- Add more links as needed -->
</div>
```

### Call-to-Action Links
Update the main CTA buttons:
```html
<!-- Hero section CTA -->
<a href="https://freebusineswebsite.com" class="inline-block bg-gradient-to-r...">
    Start Building Now
</a>

<!-- Bottom CTA section -->
<a href="https://freebusineswebsite.com" class="inline-block bg-white...">
    Get Started Free
</a>
```

## Adding Privacy and Terms Pages

1. Create new HTML files:
   - Create `privacy.html`
   - Create `terms.html`

2. Update footer links:
```html
<!-- Find this section in the footer -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <!-- Update these href attributes -->
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
If color gradients disappear, check these classes:
```html
bg-gradient-to-r from-purple-500 to-pink-500
```
Ensure all parts are present and spelled correctly.

2. **Mobile Menu Not Working**
Verify Alpine.js is loaded:
```html
<script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
```

3. **Responsive Design Issues**
Check for these prefixes in classes:
- `md:` (medium screens)
- `lg:` (large screens)
Example:
```html
class="text-4xl md:text-5xl lg:text-6xl"
```

### Tips
- Always test changes in multiple browsers
- View the page on both desktop and mobile devices
- Keep the original HTML as a backup before making changes
- Maintain the same class structure when adding new elements

Need more help? Contact support at the email provided in the footer section.