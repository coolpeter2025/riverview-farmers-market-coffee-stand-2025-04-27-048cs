# Delightful Bean Landing Page - Maintenance Guide

This guide will help you maintain and customize the Delightful Bean coffee stand landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and brand name. To update:

1. **Brand Name:**
```html
<a href="/" class="text-2xl font-bold tracking-tight text-white hover:text-amber-400">
    Delightful Bean  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update your main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Riverview Farmers Market Coffee Stand  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Locally sourced coffee with Riverview community spirit  <!-- Subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom
- `px-[size]`: Adds padding left and right
- `bg-[color]`: Sets background color

Example of modifying a button:
```html
<!-- Original -->
<a href="/" class="bg-amber-500 hover:bg-amber-600 text-gray-900 px-8 py-4">

<!-- To make button larger with different colors -->
<a href="/" class="bg-blue-500 hover:bg-blue-600 text-white px-10 py-5">
```

## Managing Links

### Navigation Links
All internal section links start with `#`:
```html
<!-- Current internal links -->
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>

<!-- To link to external page, use full URL -->
<a href="https://www.yoursite.com/features">Features</a>
```

### Store Link
Update the main call-to-action button:
```html
<a href="https://www.delightfulbean.com/" class="inline-block bg-amber-500">
    Visit Our Store  <!-- Update text and URL -->
</a>
```

### Email Links
Find and update email addresses:
```html
<!-- In contact section -->
<a href="mailto:info@delightfulbean.com">info@delightfulbean.com</a>

<!-- In footer -->
<p class="text-gray-400">info@delightfulbean.com</p>
```

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these lines to the footer's Quick Links section:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <ul class="space-y-2">
        <!-- Add these new lines -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition duration-300">Features</a></li>
    </ul>
</div>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly:
   ```html
   <!-- Link in navigation -->
   <a href="#features">Features</a>
   
   <!-- Matching section ID -->
   <section id="features" class="py-24">
   ```

2. **Responsive Design Issues**
   - Check mobile classes:
   ```html
   <!-- Example of responsive classes -->
   class="text-4xl md:text-5xl lg:text-6xl"
   <!-- text-4xl: mobile (default)
       md:text-5xl: tablet
       lg:text-6xl: desktop -->
   ```

3. **Color Consistency**
   - Main colors used:
     - Primary: `amber-400`, `amber-500`, `amber-600`
     - Background: `gray-800`, `gray-900`
     - Text: `text-white`, `text-gray-300`, `text-gray-400`

### Need Help?
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser dev tools (F12)
- Ensure all images have alt text for accessibility

Remember to test all changes across different devices and browsers before pushing to production.