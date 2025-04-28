# 101Headshots Landing Page - Maintenance Guide

This guide will help you maintain and customize the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">101Headshots</a>
```
- Replace "101Headshots" with your desired text
- Keep the classes to maintain the gradient effect

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-purple-400 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-purple-400 transition-colors duration-300">Benefits</a>
    <a href="#contact" class="hover:text-purple-400 transition-colors duration-300">Contact</a>
</div>
```
- Update text between `<a>` tags
- Maintain the `hover:text-purple-400` class for consistent hover effects

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">Kearney, Missouri Corporate Headshot Photography Services</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-8">Polished photos that give Kearney leaders a competitive edge.</p>
```
- Update heading and paragraph text as needed
- Keep responsive text classes (`text-4xl md:text-5xl lg:text-6xl`)
- Maintain gradient effect classes for the heading

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-900 p-8 rounded-2xl hover:shadow-xl hover:shadow-purple-500/10 transition-all duration-300 transform hover:scale-105">
    <i class="fas fa-camera text-4xl text-purple-400 mb-4"></i>
    <h3 class="text-xl font-bold mb-4">Professional Polish</h3>
    <p class="text-gray-400">Expert retouching and enhancement...</p>
</div>
```
- Update icon classes (e.g., `fa-camera`) using [Font Awesome](https://fontawesome.com/icons)
- Modify heading and paragraph text
- Keep hover effect classes for consistency

## Fixing Broken Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```
To update:
1. For internal sections, use `#section-id`
2. For external pages, use full URLs:
```html
<a href="https://www.yoursite.com/page">Page Name</a>
```

### Call-to-Action Buttons
Current booking links:
```html
<a href="https://www.101headshots.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-500 to-pink-500 rounded-full">Schedule Your Session</a>
```
To update:
1. Replace `https://www.101headshots.com` with your booking URL
2. Maintain all classes for consistent styling

### Email Links
Current email link:
```html
<a href="mailto:bryan@101headshots.com">bryan@101headshots.com</a>
```
To update:
1. Replace both the `href` and display text with your email address
2. Keep the `mailto:` prefix in the href

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-purple-400 transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
   - Ensure all gradient classes remain intact:
   - `bg-gradient-to-r from-purple-400 to-pink-500`
   - `bg-clip-text text-transparent` (for text gradients)

2. **Responsive Issues**
   - Check responsive classes like `md:` and `lg:`
   - Test on multiple screen sizes
   - Don't remove `hidden md:flex` from navigation

3. **Missing Hover Effects**
   - Verify transition classes are present:
   - `transition-all duration-300`
   - `hover:` classes remain on interactive elements

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Font Awesome icons at [Font Awesome](https://fontawesome.com)
- Test all links before deploying changes
- Keep a backup of the original code

Remember to test all changes in a development environment before pushing to production.