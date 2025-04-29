# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the WebAgency landing page. Follow these steps to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold text-blue-600">WebAgency</div>
```
- Replace "WebAgency" with your company name
- Adjust text size using `text-2xl` (options: text-lg, text-xl, text-3xl)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <!-- Additional menu items -->
</div>
```
- Change menu text by editing the text between `<a>` tags
- Maintain the `href` attributes matching section IDs

### Hero Section
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">
    Best Web Agency In Sydney
</h1>
<p class="text-xl md:text-2xl text-gray-600">
    Grow your business with clicks
</p>
```
- Update heading and subheading text
- Responsive sizes are defined using:
  - `text-4xl`: Mobile devices
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Tailwind CSS Tips
- Color classes follow pattern: `text-{color}-{shade}` (e.g., `text-blue-600`)
- Spacing classes use pattern: `p-{number}` for padding, `m-{number}` for margin
- Responsive prefixes: `md:` (768px), `lg:` (1024px)

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure section IDs match href values
2. For external links, replace "#" with full URL:
```html
<a href="https://your-site.com/page">Page Name</a>
```

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://fixrr.online" class="inline-block px-8 py-4 bg-blue-600">
    Start Growing Today
</a>
```
To update:
1. Replace "https://fixrr.online" with your desired URL
2. Update button text between `<a>` tags
3. Maintain all classes for consistent styling

### Social Media Links
Located in footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Additional social links -->
</div>
```
Replace "#" with your social media profiles:
```html
<a href="https://twitter.com/your-profile">
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace placeholder links in the footer:
```html
<!-- Original Code -->
<li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>

<!-- Updated Code -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="text-gray-400 hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Verify section IDs match href attributes
- Section IDs should not contain spaces
- Example: `href="#contact"` matches `id="contact"`

2. **Responsive Design Issues**
- Check responsive prefixes are correct:
  ```html
  class="text-xl md:text-2xl lg:text-3xl"
  ```
- Test on different screen sizes using browser dev tools

3. **Icon Display Problems**
- Verify Font Awesome CSS is loaded:
  ```html
  <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
  ```
- Check icon class names match Font Awesome 6 syntax

### Need Help?
- Inspect elements using browser dev tools (F12)
- Compare changes against original code
- Test all links after updates
- Verify Tailwind CSS and Font Awesome CDN links are accessible

Remember to always backup your code before making changes and test on multiple devices after updates.