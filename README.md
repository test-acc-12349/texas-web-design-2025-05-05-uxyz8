# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. It's written for beginners and provides step-by-step instructions for common maintenance tasks.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Sections
The landing page is divided into these key sections:
- Header (Navigation)
- Hero Section
- Features
- Benefits
- FAQ
- Contact
- Footer

### Updating Text Content

#### Hero Section
Located near the top of the page, find these lines:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```
To update:
1. Replace the text between `<h1>` tags for the main heading
2. Replace the text between `<p>` tags for the subheading

#### Features Section
Find the features cards (there are three) that look like this:
```html
<h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
<p class="text-gray-600">Premium hosting included with every website package.</p>
```
To update:
1. Replace the text between `<h3>` tags for feature titles
2. Replace the text between `<p>` tags for feature descriptions

### Understanding Tailwind Classes

Key class patterns used in this page:

#### Spacing Classes
- `px-6`: Adds horizontal padding
- `py-4`: Adds vertical padding
- `mb-6`: Adds bottom margin
- `space-x-8`: Adds horizontal spacing between elements

#### Responsive Classes
- `md:text-5xl`: Applies style at medium screen sizes
- `lg:text-6xl`: Applies style at large screen sizes
- `hidden md:flex`: Hidden on mobile, flex on medium screens

#### Color Classes
- `text-blue-600`: Blue text color
- `bg-white`: White background
- `hover:bg-blue-700`: Blue background on hover

## Managing Links

### Navigation Menu Links
Located in the header section:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Contact</a>
</div>
```

To update internal links:
1. Locate the `href` attribute
2. Update the value to match your section ID
   - Example: `href="#new-section"`

### External Links
Current placeholder links to update:
```html
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600 text-white rounded-full">
```
Replace `https://twd.com` with your actual website URL.

### Email Links
Located in the contact section:
```html
<a href="mailto:admin@twd.com" class="text-lg hover:underline">admin@twd.com</a>
```
Update both the `href="mailto:..."` and the displayed email address.

## Adding Privacy and Terms Pages

### Footer Links Setup
Located in the footer section:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues**
   - Check mobile view using browser dev tools
   - Verify `md:` and `lg:` classes are properly set

3. **Style Inconsistencies**
   - Maintain consistent color classes (e.g., `text-blue-600`)
   - Keep consistent spacing patterns (e.g., `px-6 py-4`)

### Need Help?
- Check Tailwind CSS documentation for class references
- Validate HTML using W3C Validator
- Test all links after making changes
- View page in multiple browsers and screen sizes

Remember to always make a backup of your files before making significant changes.