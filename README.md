# UWB.ai Landing Page - Maintenance Guide

This guide will help you maintain and customize the UWB.ai landing page. Whether you're new to web development or just getting started, follow these instructions to make updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">UWB.ai</a>
```
- Replace "UWB.ai" with your desired text
- Keep the classes unchanged to maintain the gradient effect

### Hero Section
Located at the top of the page with the main headline:

```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold mb-6 bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">Build An Amazing Website In 3 Minutes</h1>
```
- Update the text between the `<h1>` tags
- The classes control:
  - `text-5xl`: Base text size
  - `md:text-6xl`: Size on medium screens
  - `lg:text-7xl`: Size on large screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-800 p-8 rounded-2xl hover:bg-gray-700/50 transition-all duration-300 hover:-translate-y-1 hover:shadow-xl hover:shadow-purple-500/10">
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description text.</p>
</div>
```
- Update the text in `<h3>` for feature titles
- Update the text in `<p>` for descriptions
- Maintain the classes for consistent styling

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-300 hover:text-white transition-colors duration-300">FAQ</a>
</div>
```
To update:
1. Locate the `href` attribute
2. Replace "#features" with your new link
   - Use "#section-id" for same-page links
   - Use full URLs for external links (e.g., "https://example.com")

### Call-to-Action Links
Find and update all instances of:
```html
<a href="https://uwb.com" class="bg-gradient-to-r from-purple-600 to-pink-600...">
```
- Replace "https://uwb.com" with your actual website URL
- Maintain all classes to preserve the button styling

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add links:
1. Create privacy.html and terms.html in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Gradient Effects**
   - Ensure all gradient classes remain unchanged:
   - `bg-gradient-to-r`
   - `from-purple-500/600`
   - `to-pink-500/600`

2. **Responsive Issues**
   - Check that responsive classes are preserved:
   - `md:` prefix for medium screens
   - `lg:` prefix for large screens

3. **Link Problems**
   - Verify all `href` attributes have:
   - Correct file paths for internal links
   - Complete URLs for external links
   - Proper section IDs for same-page navigation

### Need Help?
- Double-check your changes against the original code
- Ensure all opening tags have corresponding closing tags
- Maintain all Tailwind CSS classes exactly as shown
- Test the page at different screen sizes

Remember to always make a backup of your files before making changes, and test your updates in a browser to ensure everything works as expected.