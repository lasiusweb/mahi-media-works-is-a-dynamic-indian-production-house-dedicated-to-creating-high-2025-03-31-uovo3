# Mahi Media Works Landing Page - Maintenance Guide

This guide will help you maintain and customize the Mahi Media Works landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Name/Logo**
```html
<!-- Located at the top of the page -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Mahi Media
</a>
```
- Replace "Mahi Media" with your company name
- Keep the existing classes to maintain the gradient effect

### Hero Section
The main banner section contains your primary heading and call-to-action:

1. **Main Heading**
```html
<h1 class="text-4xl md:text-6xl font-bold leading-tight tracking-tighter mb-8 bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Mahi Media Works is a dynamic Indian production house dedicated to creating high
</h1>
```
- Update the text between the `<h1>` tags
- Don't remove the classes as they control:
  - `text-4xl`: Size on mobile devices
  - `md:text-6xl`: Larger size on medium screens
  - `bg-gradient-to-r`: Creates the gradient effect

2. **Subheading**
```html
<p class="text-xl md:text-2xl text-gray-300 max-w-3xl mx-auto mb-12">
    I am truly grateful to Mahi Media Works for believing in me
</p>
```
- Replace the text while maintaining the paragraph tags
- Keep the classes for consistent styling

### Tailwind CSS Class Guide
Common classes used throughout the page:

- Text Sizes:
  - `text-xl`: Large text
  - `text-2xl`: Extra large text
  - `md:text-4xl`: Different size on medium screens
  
- Colors:
  - `text-gray-300`: Light gray text
  - `bg-gray-900`: Dark background
  - `from-purple-500 to-pink-500`: Gradient colors

- Spacing:
  - `mb-8`: Margin bottom
  - `py-24`: Padding top and bottom
  - `px-4`: Padding left and right

## Managing Links

### Navigation Menu Links
Located in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-300 hover:text-white transition-colors duration-300">Home</a>
    <a href="#" class="text-gray-300 hover:text-white transition-colors duration-300">About</a>
    <a href="#" class="text-gray-300 hover:text-white transition-colors duration-300">Projects</a>
    <a href="#" class="text-gray-300 hover:text-white transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. Replace the `#` in `href="#"` with your page URLs
2. Example: `href="about.html"` or `href="https://example.com/about"`
3. Keep the existing classes for hover effects

### Footer Links
Located at the bottom of the page:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Projects</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Contact</a></li>
</ul>
```

Update these links the same way as the navigation menu links.

## Adding Privacy and Terms Pages

### Step 1: Add Links to Footer
Insert new list items in the footer links section:
```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create Policy Pages
1. Create two new files: `privacy.html` and `terms.html`
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between them

Example structure for policy pages:
```html
<!-- privacy.html or terms.html -->
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<!-- Copy head section from index.html -->

<body class="bg-gray-900 text-gray-100 font-inter antialiased">
    <!-- Copy header section -->
    
    <main class="container mx-auto px-4 py-24">
        <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>

    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Gradient Text**
   - Ensure all gradient text elements have these classes:
     ```
     bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent
     ```

2. **Responsive Issues**
   - Check that you've kept the `md:` prefixed classes
   - Test on multiple screen sizes using browser dev tools

3. **Link Problems**
   - Verify file paths are correct
   - Use relative paths for internal links
   - Use full URLs for external links

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).