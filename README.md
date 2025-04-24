# Albert Park Landing Page - Maintenance Guide

This guide will help you maintain and customize the Albert Park accounting services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

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
<!-- Find this section in the header -->
<div class="text-2xl font-bold bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Albert Park  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subtext:
```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent">
    Your financial success is our bottom line  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Professional accounting services...  <!-- Subheading text -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-{size}`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-{number}`: Margin bottom spacing (4, 8, 12, etc.)
- `py-{number}`: Padding top and bottom
- `px-{number}`: Padding left and right
- `bg-{color}-{shade}`: Background colors
- `hover:scale-105`: Enlarges element on hover
- `transition-{type}`: Adds smooth transitions

## Managing Links

### Navigation Menu Links
```html
<!-- Desktop Navigation -->
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Internal section link -->
    <a href="#benefits">Benefits</a>  <!-- Internal section link -->
    <a href="#contact">Contact</a>    <!-- Internal section link -->
</div>

<!-- Mobile Navigation -->
<div x-show="isOpen" class="md:hidden mt-4 space-y-4">
    <!-- Update both desktop and mobile links to match -->
</div>
```

### Call-to-Action Links
```html
<!-- Main CTA Button -->
<a href="https://theaccountants.com" class="inline-block bg-gradient-to-r...">
    Transform Your Finances  <!-- Update href and text -->
</a>
```

### Footer Links
Current placeholder links to update:
```html
<!-- Services Section -->
<ul class="space-y-2 text-gray-400">
    <li><a href="#">Tax Optimization</a></li>  <!-- Add proper href -->
    <li><a href="#">Cloud Accounting</a></li>
    <li><a href="#">Financial Reporting</a></li>
</ul>

<!-- Company Section -->
<ul class="space-y-2 text-gray-400">
    <li><a href="#">About Us</a></li>  <!-- Add proper href -->
    <li><a href="#">Careers</a></li>
    <li><a href="#">Blog</a></li>
</ul>
```

## Adding Privacy and Terms Pages

### 1. Update Footer Legal Links
```html
<!-- Find this section in the footer -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
        <li><a href="cookies.html" class="hover:text-white transition-colors duration-300">Cookie Policy</a></li>
    </ul>
</div>
```

### 2. Create Matching Pages
Create `privacy.html` and `terms.html` in the same directory as `index.html`. Use the same styling classes for consistency:

```html
<!-- privacy.html template -->
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100 font-sans antialiased">
    <!-- Copy header from index.html -->
    
    <main class="pt-24 px-6">
        <div class="container mx-auto">
            <h1 class="text-4xl font-bold mb-8">Privacy Policy</h1>
            <!-- Add privacy policy content -->
        </div>
    </main>

    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links**
   - Ensure section IDs match href attributes
   - Check for typos in href values
   - Verify that all sections have unique IDs

2. **Responsive Design Issues**
   - Keep the `md:` and `lg:` prefixed classes for proper responsive behavior
   - Test on multiple screen sizes using browser dev tools
   - Don't remove the `container` class from main sections

3. **Gradient Text Not Showing**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-500 bg-clip-text text-transparent
     ```

4. **Mobile Menu Not Working**
   - Verify Alpine.js is properly loaded
   - Check that `x-data` and `x-show` attributes are present
   - Ensure JavaScript is enabled in the browser

For additional help, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Alpine.js Documentation](https://alpinejs.dev/docs)