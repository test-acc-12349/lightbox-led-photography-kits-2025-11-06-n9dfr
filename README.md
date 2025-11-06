# Lightbox LED Photography Landing Page - Maintenance & Customization Guide

A comprehensive guide for maintaining, updating, and customizing your Lightbox LED Photography landing page. This guide is designed for beginners with no prior coding experience.

---

## Table of Contents

1. [Overview](#overview)
2. [Understanding the Page Structure](#understanding-the-page-structure)
3. [Updating Text Content](#updating-text-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Updating Links](#fixing-and-updating-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Common Tasks & Troubleshooting](#common-tasks--troubleshooting)
8. [Best Practices](#best-practices)

---

## Overview

Your landing page is built using:
- **HTML**: The structure and content of the page
- **Tailwind CSS**: A utility-first CSS framework for styling and responsive design
- **Font Awesome**: Icons used throughout the page (lightbulbs, stars, arrows, etc.)
- **JavaScript**: Interactive features like mobile menu toggle and accordions

This guide will help you make changes without breaking the design or functionality.

---

## Understanding the Page Structure

### Main Sections of Your Landing Page

Your landing page consists of these key sections:

| Section | ID | Purpose | Line Location |
|---------|----|---------|----|
| Announcement Bar | N/A | Displays shipping/guarantee message at top | Lines 73-75 |
| Navigation Header | `<header>` | Sticky menu with logo and navigation links | Lines 77-142 |
| Hero Section | `#home` | Large banner with main headline and CTA buttons | Lines 144-171 |
| Features Section | `#features` | Three feature cards with icons | Lines 173-227 |
| Benefits Section | `#benefits` | Three benefit sections with images | Lines 229-336 |
| About Us Section | `#about` | Company story and statistics | Lines 338-387 |
| Testimonials Section | `#testimonials` | Customer reviews with ratings | Lines 389-477 |
| FAQ Section | `#faq` | Expandable question/answer pairs | Lines 479-619 |
| CTA Section | N/A | Large call-to-action banner | Lines 621-656 |
| Contact Section | `#contact` | Contact information and quick links | Lines 658-717 |
| Footer | `<footer>` | Company info, links, newsletter, policies | Lines 719-836 |

### How the Page Works

1. **Navigation anchors** (the `#` symbols) link to different sections
2. **Tailwind classes** control all styling and responsive behavior
3. **JavaScript** handles interactive features
4. **External images** come from Unsplash (a free image service)

---

## Updating Text Content

### What You Need to Know About Text

Text content in HTML is placed between opening and closing tags. For example:

```html
<h1>This is a heading</h1>
<p>This is a paragraph</p>
```

To update text, you simply replace what's between the tags while keeping the tags themselves intact.

### Step-by-Step: Updating Common Text Elements

#### 1. **Changing the Main Headline (Hero Section)**

**Location:** Lines 155-157

**Current code:**
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Lightbox LED Photography Kits
</h1>
```

**To change it:**
1. Find the text "Lightbox LED Photography Kits"
2. Replace it with your desired headline
3. Keep the `<h1>` tags and all the classes exactly as they are

**Example - changing to a different headline:**
```html
<h1 class="text-4xl md:text-6xl font-bold text-white mb-6 leading-tight tracking-tight">
    Professional Photography Lighting Solutions
</h1>
```

#### 2. **Changing the Hero Subtitle**

**Location:** Lines 158-160

**Current code:**
```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed font-light">
    Take great photos get more sales
</p>
```

**To change it:**
1. Replace "Take great photos get more sales" with your new text
2. Keep all the `class` attributes unchanged

**Example:**
```html
<p class="text-xl md:text-2xl text-gray-100 mb-8 leading-relaxed font-light">
    Professional lighting. Instant setup. Proven results.
</p>
```

#### 3. **Changing Feature Card Titles and Descriptions**

**Location:** Lines 197-227 (three feature cards)

**First feature card example - current code:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Professional Lighting</h3>
<p class="text-gray-600 leading-relaxed">
    Our advanced LED technology delivers studio-quality lighting...
</p>
```

**To change it:**
1. Replace "Professional Lighting" with your new title
2. Replace the paragraph text with your description
3. Keep all HTML tags and classes the same

**Example:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Studio-Quality LED Lighting</h3>
<p class="text-gray-600 leading-relaxed">
    Advanced LED technology that delivers professional results every time...
</p>
```

#### 4. **Updating Benefit Section Text**

**Location:** Lines 270-295 (first benefit section)

**Current code:**
```html
<h3 class="text-3xl font-bold text-gray-900 mb-4">Professional Photos</h3>
<p class="text-lg text-gray-700 mb-6 leading-relaxed">
    Achieve gallery-quality product photography without hiring expensive photographers...
</p>
```

**To change it:**
1. Replace the heading text
2. Replace the paragraph text
3. Update bullet points if needed (see next section)

#### 5. **Updating Bullet Points in Lists**

**Location:** Throughout the page (e.g., lines 285-291)

**Current code:**
```html
<ul class="space-y-4 mb-8">
    <li class="flex items-start">
        <i class="fas fa-star text-yellow-500 mr-3 mt-1 flex-shrink-0"></i>
        <span class="text-gray-700"><strong>Studio Quality:</strong> Achieve professional lighting setups...</span>
    </li>
</ul>
```

**To change it:**
1. Replace the text after `<strong>` and in the `<span>`
2. Keep the `<i>` tag and all classes exactly the same

**Example:**
```html
<li class="flex items-start">
    <i class="fas fa-star text-yellow-500 mr-3 mt-1 flex-shrink-0"></i>
    <span class="text-gray-700"><strong>Premium Quality:</strong> Achieve professional-grade results instantly...</span>
</li>
```

#### 6. **Updating Testimonials**

**Location:** Lines 431-477 (four testimonial cards)

**Current code example:**
```html
<p class="text-gray-700 mb-6 leading-relaxed text-base">
    "The Lightbox LED kit completely transformed my Etsy shop..."
</p>
<div>
    <p class="font-semibold text-gray-900">Sarah Mitchell</p>
    <p class="text-sm text-gray-600">Handmade Jewelry Shop Owner, Etsy</p>
</div>
```

**To change it:**
1. Replace the testimonial quote text
2. Replace the customer name
3. Replace the customer title/business

#### 7. **Updating FAQ Answers**

**Location:** Lines 551-619 (FAQ section)

**Current code example:**
```html
<button class="accordion-button w-full flex justify-between items-center p-6 bg-white hover:bg-gray-50 transition-colors duration-300 focus:outline-none" onclick="toggleAccordion(this)">
    <span class="text-lg font-semibold text-gray-900 text-left">What's included in the Lightbox LED Photography Kit?</span>
    <i class="fas fa-chevron-down text-gray-600 transition-transform duration-300"></i>
</button>
<div class="accordion-content bg-gray-50 border-t border-gray-200">
    <div class="p-6 text-gray-700 leading-relaxed">
        <p class="mb-4">Our complete Lightbox LED Photography Kit includes:</p>
        <ul class="list-disc list-inside space-y-2 ml-2">
            <li>Two professional-grade LED light panels...</li>
        </ul>
    </div>
</div>
```

**To change it:**
1. Replace the question text in the `<span>`
2. Replace the answer content inside the `.accordion-content` div
3. Keep all HTML structure and classes the same

#### 8. **Updating Footer Text**

**Location:** Lines 755-836

**Current code example:**
```html
<p class="text-gray-400 text-sm leading-relaxed mb-6">
    Professional LED photography lighting kits that help businesses...
</p>
```

**To change it:**
1. Replace the paragraph text
2. Keep the `<p>` tag and classes the same

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind CSS

Tailwind CSS is a "utility-first" framework that uses predefined classes to style elements. Instead of writing custom CSS, you combine classes.

**Example:**
```html
<h1 class="text-4xl font-bold text-white mb-6">Heading</h1>
```

This means:
- `text-4xl` = Large font size
- `font-bold` = Bold text
- `text-white` = White text color
- `mb-6` = Margin (space) at bottom

### Common Tailwind Classes Used in Your Landing Page

#### Text & Font Classes

| Class | What It Does | Examples |
|-------|-------------|----------|
| `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl` | Font size | Larger numbers = bigger text |
| `font-light`, `font-normal`, `font-semibold`, `font-bold` | Font weight (thickness) | `font-bold` makes text thicker |
| `text-white`, `text-gray-900`, `text-gray-700`, `text-yellow-500` | Text color | `text-white` = white, `text-gray-900` = dark gray |
| `leading-relaxed`, `leading-tight` | Line spacing | How much space between lines |
| `tracking-tight` | Letter spacing | Space between individual letters |

#### Spacing Classes

| Class | What It Does | Examples |
|-------|-------------|----------|
| `mb-4`, `mb-6`, `mb-8`, `mb-12` | Margin bottom (space below element) | Higher number = more space |
| `mt-4`, `mt-6` | Margin top (space above element) | Higher number = more space |
| `px-4`, `px-6`, `px-8` | Padding horizontal (space inside, left/right) | Higher number = more space |
| `py-4`, `py-6` | Padding vertical (space inside, top/bottom) | Higher number = more space |
| `p-8`, `p-12` | Padding all sides | Higher number = more space |

#### Color Classes

| Class | Color |
|-------|-------|
| `text-white` | White text |
| `text-gray-900` | Very dark gray text |
| `text-gray-700` | Medium gray text |
| `text-gray-600` | Lighter gray text |
| `text-yellow-500` | Yellow text |
| `bg-white` | White background |
| `bg-gray-50` | Very light gray background |
| `bg-gray-900` | Very dark gray background |
| `bg-yellow-500` | Yellow background |
| `border-gray-200` | Gray border |

#### Responsive Classes

Tailwind uses prefixes to make designs responsive:
- `md:` = Medium screens and up (tablets, desktops)
- `sm:` = Small screens and up (larger phones)

**Example:**
```html
<h1 class="text-4xl md:text-6xl">
```
This means:
- On small/mobile screens: Use `text-4xl` (smaller)
- On medium screens and larger: Use `text-6xl` (bigger)

### How to Modify Tailwind Classes - Common Tasks

#### Task 1: Make Text Larger or Smaller

**Current code:**
```html
<h2 class="text-3xl md:text-4xl font-bold">
    Why Choose Our Lighting Kits?
</h2>
```

**To make it larger:**
- Change `text-3xl` to `text-4xl` (mobile size)
- Change `md:text-4xl` to `md:text-5xl` (desktop size)

**Result:**
```html
<h2 class="text-4xl md:text-5xl font-bold">
    Why Choose Our Lighting Kits?
</h2>
```

#### Task 2: Change Text Color

**Current code:**
```html
<p class="text-gray-600">Some text here</p>
```

**Available color options:**
- `text-white` = white
- `text-gray-900` = very dark gray
- `text-gray-700` = medium dark gray
- `text-gray-600` = medium gray
- `text-yellow-500` = yellow
- `text-blue-600` = blue
- `text-green-600` = green

**To change to a different color:**
```html
<p class="text-gray-700">Some text here</p>
```

#### Task 3: Add or Remove Spacing

**Current code:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-3">Feature Title</h3>
<p class="text-gray-600 mb-6">Description text</p>
```

**To add more space below the heading:**
- Change `mb-3` to `mb-6` (more space)

**Result:**
```html
<h3 class="text-xl font-bold text-gray-900 mb-6">Feature Title</h3>
<p class="text-gray-600 mb-6">Description text</p>
```

#### Task 4: Change Background Colors

**Current code:**
```html
<div class="bg-white border border-gray-200 rounded-lg p-8">
```

**To change to light gray background:**
```html
<div class="bg-gray-50 border border-gray-200 rounded-lg p-8">
```

#### Task 5: Adjust Button Styling

**Current code:**
```html
<a href="#" class="px-8 py-4 bg-yellow-500 text-gray-900 font-bold text-lg rounded-lg">
    Buy Now
</a>
```

**To make button text larger:**
```html
<a href="#" class="px-8 py-4 bg-yellow-500 text-gray-900 font-bold text-xl rounded-lg">
    Buy Now
</a>
```

**To make button wider:**
```html
<a href="#" class="px-12 py-4 bg-yellow-500 text-gray-900 font-bold text-lg rounded-lg">
    Buy Now
</a>
```

### Maintaining Responsive Design

**Important:** When you see both `text-4xl` and `md:text-6xl`, this means:
- Keep BOTH classes
- The first one applies to mobile/small screens
- The second one (with `md:`) applies to medium screens and larger

**Example - DO THIS:**
```html
<h1 class="text-4xl md:text-6xl font-bold">Heading</h1>
```

**Example - DON'T DO THIS (breaks mobile design):**
```html
<h1 class="text-6xl font-bold">Heading</h1>
```

---

## Fixing and Updating Links

### Understanding Links in HTML

A link in HTML looks like this:
```html
<a href="https://example.com">Click Here</a>
```

- `<a>` = anchor (link) tag
- `href="..."` = where the link goes
- Text between tags = what users see and click on

### Types of Links on Your Page

Your landing page has three types of links:

1. **Internal anchors** - Links to sections on the same page (start with `#`)
2. **External links** - Links to other websites (start with `http://` or `https://`)
3. **File links** - Links to other pages in your project (like `privacy.html`)

### Current Links That Need Attention

#### 1. **Navigation Menu Links (Working Correctly)**

**Location:** Lines 99-105 (desktop) and 117-123 (mobile)

**Current code:**
```html
<a href="#home" class="text-gray-700 hover:text-gray-900">Home</a>
<a href="#features" class="text-gray-700 hover:text-gray-900">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-gray-900">Benefits</a>
<a href="#about" class="text-gray-700 hover:text-gray-900">About</a>
<a href="#testimonials" class="text-gray-700 hover:text-gray-900">Testimonials</a>
<a href="#faq" class="text-gray-700 hover:text-gray-900">FAQ</a>
<a href="#contact" class="text-gray-700 hover:text-gray-900">Contact</a>
```

**Status:** ✅ These are correct - they link to sections with matching IDs on the page.

#### 2. **"Buy Now" and "Get Started" Buttons (Need Your Stripe Link)**

**Locations:**
- Line 108 (header desktop)
- Line 126 (header mobile)
- Line 162 (hero section)
- Line 296 (benefits section)
- Line 322 (benefits section)
- Line 340 (benefits section)
- Line 639 (CTA section)
- Line 643 (CTA section)
- Line 695 (contact section)

**Current code:**
```html
<a href="https://checkout.stripe.com/c/pay/cs_live_b1n4XezSnTLY27IeaApXnYo6UCTeOQILKYH2G1AIQ4TpgZCgqGVsKH4f4S#fidnandhYHdWcXxpYCc%2FJ2FgY2RwaXEnKSdkdWxOYHwnPyd1blppbHNgWjA0VF18NTROMlA8Y2g0dG9Tc1NpYmxEVU5GZmZsPT1cQVZccjByUGBvfFxzSGZJQENzQnNgNnQ2YjYwN0NcSWpMVFAxa2lmSjBXa0RCZHdBTVU2SnAxVUBgNTVzQE53aFFjUCcpJ2N3amhWYHdzYHcnP3F3cGApJ2dkZm5id2pwa2FGamlqdyc%2FJyZjY2NjY2MnKSdpZHxqcHFRfHVgJz8naHBpcWxabHFgaCcpJ2BrZGdpYFVpZGZgbWppYWB3dic%2FcXdwYHgl">
    Buy Now
</a>
```

**What this is:** This is a Stripe payment link (for processing purchases).

**To update it:**

1. **Get your Stripe checkout link:**
   - Log in to your Stripe account
   - Go to Payment Links section
   - Create a new payment link for your product
   - Copy the full URL

2. **Replace the current link:**
   - Find each "Buy Now" or "Get Started" button
   - Replace the entire URL in the `href="..."` with your new Stripe link
   - Keep the text ("Buy Now", "Get Started", "Order Now") the same

**Example - After updating:**
```html
<a href="https://checkout.stripe.com/c/pay/YOUR_NEW_STRIPE_LINK_HERE">
    Buy Now
</a>
```

**How many to update:** 7 locations total

#### 3. **Footer Links (Mostly Placeholders)**

**Location:** Lines 783-836

**Current code example:**
```html
<a href="#" class="text-gray-400 hover:text-yellow-500">Photography Kits</a>
<a href="#" class="text-gray-400 hover:text-yellow-500">Accessories</a>
<a href="blog.html" class="text-gray-400 hover:text-yellow-500">Blog</a>
<a href="privacy.html" class="text-gray-400 hover:text-yellow-500">Privacy Policy</a>
<a href="terms.html" class="text-gray-400 hover:text-yellow-500">Terms of Service</a>
```

**Status:** 
- ✅ `blog.html`, `privacy.html`, `terms.html` are correct (see next section)
- ⚠️ Links with `href="#"` are placeholders that don't go anywhere

**To fix placeholder links:**

Option 1: Link to a section on the page
```html
<a href="#features" class="text-gray-400 hover:text-yellow-500">Photography Kits</a>
```

Option 2: Link to an external URL
```html
<a href="https://example.com/accessories" class="text-gray-400 hover:text-yellow-500">Accessories</a>
```

Option 3: Remove the link if you don't have a destination yet
```html
<span class="text-gray-400">Accessories</span>
```

#### 4. **Contact Email Link**

**Location:** Line 701

**Current code:**
```html
<a href="mailto:test@test.com" class="text-gray-600 hover:text-yellow-500 transition-colors duration-300">test@test.com</a>
```

**To update it:**
1. Replace `test@test.com` with your actual email address (appears twice)
2. Keep `mailto:` exactly as it is

**Example:**
```html
<a href="mailto:support@lightboxled.com" class="text-gray-600 hover:text-yellow-500 transition-colors duration-300">support@lightboxled.com</a>
```

#### 5. **Social Media Links**

**Location:** Lines 778-791 (footer)

**Current code:**
```html
<a href="#" class="w-10 h-10 bg-gray-800 rounded-full flex items-center justify-center hover:bg-yellow-500">
    <i class="fab fa-facebook-f"></i>
</a>
```

**To update it:**
1. Replace `#` with your actual social media URL
2. Keep all the classes the same

**Examples:**
```html
<!-- Facebook -->
<a href="https://facebook.com/yourusername" class="...">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- Twitter -->
<a href="https://twitter.com/yourusername" class="...">
    <i class="fab fa-twitter"></i>
</a>

<!-- Instagram -->
<a href="https://instagram.com/yourusername" class="...">
    <i class="fab fa-instagram"></i>
</a>

<!-- YouTube -->
<a href="https://youtube.com/yourchannel" class="...">
    <i class="fab fa-youtube"></i>
</a>
```

### Quick Reference: All Links That Need Updating

| Link Type | Location | Current Status | Action Needed |
|-----------|----------|-----------------|---------------|
| Navigation anchors | Lines 99-105, 117-123 | ✅ Working | No action needed |
| Buy/Get Started buttons | 7 locations | ⚠️ Placeholder | Replace with your Stripe link |
| Email link | Line 701 | ⚠️ Placeholder | Replace with your email |
| Social media | Lines 778-791 | ⚠️ Placeholder | Replace with your profiles |
| Footer product links | Lines 785-788 | ⚠️ Placeholder | Link to actual pages |
| Privacy Policy | Line 824 | ✅ Ready | See next section |
| Terms of Service | Line 825 | ✅ Ready | See next section |
| Blog | Line 823 | ✅ Ready | Create blog.html file |

---

## Adding Privacy and Terms Pages

### Overview

Your landing page already has links to `privacy.html` and `terms.html` in the footer (lines 824-825). You need to create these files.

### What Are Privacy and Terms Pages?

- **Privacy Policy**: Explains how you collect and use customer data
- **Terms of Service**: Legal rules for using your website and buying products

These are legally important for any business website.

### Step 1: Create the Privacy Policy Page

**File to create:** `privacy.html` (in the same folder as `index.html`)

**Basic template for privacy.html:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy - Lightbox LED Photography">
    <title>Privacy Policy - Lightbox LED Photography</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header (Same as index.html) -->
    <header class="sticky top-0 z-40 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16 md:h-20">
                <div class="flex items-center">
                    <a href="index.html" class="text-2xl font-bold text-gray-900 flex items-center">
                        <i class="fas fa-lightbulb text-yellow-500 mr-2"></i>
                        <span class="hidden sm:inline">Lightbox LED</span>
                        <span class="sm:hidden">LED</span>
                    </a>
                </div>
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="index.html#home" class="text-gray-700 hover:text-gray-900 font-medium">Home</a>
                    <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium">Features</a>
                    <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium">Contact</a>
                </nav>
                <a href="index.html" class="hidden sm:inline-block px-6 py-2 bg-yellow-500 text-gray-900 font-semibold rounded-lg hover:bg-yellow-400">
                    Back to Home
                </a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2024</p>

            <div class="bg-white rounded-lg p-8 md:p-12 space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Lightbox LED Photography ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">We may collect information about you in a variety of ways. The information we may collect on the Site includes:</p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 ml-4">
                        <li><strong>Personal Data:</strong> Name, email address, phone number, shipping address, billing address</li>
                        <li><strong>Payment Information:</strong> Credit card details (processed securely through Stripe)</li>
                        <li><strong>Usage Data:</strong> Pages visited, time spent, links clicked, referring source</li>
                        <li><strong>Device Information:</strong> Browser type, operating system, device type</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. How We Use Your Information</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">We use the information we collect in the following ways:</p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 ml-4">
                        <li>To process your orders and deliver products</li>
                        <li>To send you order confirmations and shipping updates</li>
                        <li>To respond to your inquiries and customer service requests</li>
                        <li>To improve our website and services</li>
                        <li>To send promotional emails (with your consent)</li>
                        <li>To prevent fraud and ensure security</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Information Sharing</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We do not sell, trade, or rent your personal information to third parties. We may share information with:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 ml-4 mt-4">
                        <li>Service providers (payment processors, shipping companies, email services)</li>
                        <li>Legal authorities when required by law</li>
                        <li>Business partners with your consent</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Data Security</h2>
                    <p class="text-gray-700 leading-relaxed">
                        We implement appropriate technical and organizational measures to protect your personal data against unauthorized access, alteration, disclosure, or destruction. Your payment information is processed securely through Stripe and is never stored on our servers.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Your Rights</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">You have the right to:</p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 ml-4">
                        <li>Access your personal data</li>
                        <li>Correct inaccurate data</li>
                        <li>Request deletion of your data</li>
                        <li>Opt-out of marketing communications</li>
                        <li>Request a copy of your data</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Contact Us</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:support@lightboxled.com" class="text-yellow-500 hover:text-yellow-600">support@lightboxled.com</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer (Same as index.html) -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 mb-4">
                &copy; <span id="year">2024</span> Lightbox LED Photography. All rights reserved.
            </p>
            <div class="flex justify-center space-x-6 text-sm">
                <a href="privacy.html" class="text-gray-400 hover:text-yellow-500">Privacy Policy</a>
                <a href="terms.html" class="text-gray-400 hover:text-yellow-500">Terms of Service</a>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

### Step 2: Create the Terms of Service Page

**File to create:** `terms.html` (in the same folder as `index.html`)

**Basic template for terms.html:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service - Lightbox LED Photography">
    <title>Terms of Service - Lightbox LED Photography</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, sans-serif;
        }
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Navigation Header -->
    <header class="sticky top-0 z-40 bg-white border-b border-gray-200 shadow-sm">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16 md:h-20">
                <div class="flex items-center">
                    <a href="index.html" class="text-2xl font-bold text-gray-900 flex items-center">
                        <i class="fas fa-lightbulb text-yellow-500 mr-2"></i>
                        <span class="hidden sm:inline">Lightbox LED</span>
                        <span class="sm:hidden">LED</span>
                    </a>
                </div>
                <nav class="hidden md:flex items-center space-x-8">
                    <a href="index.html#home" class="text-gray-700 hover:text-gray-900 font-medium">Home</a>
                    <a href="index.html#features" class="text-gray-700 hover:text-gray-900 font-medium">Features</a>
                    <a href="index.html#contact" class="text-gray-700 hover:text-gray-900 font-medium">Contact</a>
                </nav>
                <a href="index.html" class="hidden sm:inline-block px-6 py-2 bg-yellow-500 text-gray-900 font-semibold rounded-lg hover:bg-yellow-400">
                    Back to Home
                </a>
            </div>
        </div>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24 bg-gray-50">
        <div class="max-w-4xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            <p class="text-gray-600 mb-8">Last updated: January 2024</p>

            <div class="bg-white rounded-lg p-8 md:p-12 space-y-8">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Agreement to Terms</h2>
                    <p class="text-gray-700 leading-relaxed">
                        By accessing and using this website, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on Lightbox LED's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 ml-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials on Lightbox LED's website are provided on an 'as is' basis. Lightbox LED makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p class="text-gray-700 leading-relaxed">
                        In no event shall Lightbox LED or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Lightbox LED's website.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p class="text-gray-700 leading-relaxed">
                        The materials appearing on Lightbox LED's website could include technical, typographical, or photographic errors. Lightbox LED does not warrant that any of the materials on its website are accurate, complete, or current. Lightbox LED may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Lightbox LED has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Lightbox LED of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p class="text-gray-700 leading-relaxed">
                        Lightbox LED may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Governing Law</h2>
                    <p class="text-gray-700 leading-relaxed">
                        These terms and conditions are governed by and construed in accordance with the laws of the United States, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Product Warranty</h2>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        All Lightbox LED products come with the following warranty:
                    </p>
                    <ul class="list-disc list-inside space-y-2 text-gray-700 ml-4">
                        <li><strong>30-Day Money-Back Guarantee:</strong> If you're not satisfied with your purchase, return it within 30 days for a full refund</li>
                        <li><strong>2-Year Warranty:</strong> Manufacturing defects are covered for 2 years from the date of purchase</li>
                        <li><strong>Free Replacement:</strong> Any defective components will be replaced free of charge during the warranty period</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Contact Information</h2>
                    <p class="text-gray-700 leading-relaxed">
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="text-gray-700 mt-4">
                        <strong>Email:</strong> <a href="mailto:support@lightboxled.com" class="text-yellow-500 hover:text-yellow-600">support@lightboxled.com</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 text-center">
            <p class="text-gray-400 mb-4">
                &copy; <span id="year">2024</span> Lightbox LED Photography. All rights reserved.
            </p>
            <div class="flex justify-center space-x-6 text-sm">
                <a href="privacy.html" class="text-gray-400 hover:text-yellow-500">Privacy Policy</a>
                <a href="terms.html" class="text-gray-400 hover:text-yellow-500">Terms of Service</a>
            </div>
        </div>
    </footer>

    <script>
        document.getElementById('year').textContent = new Date().getFullYear();
    </script>
</body>
</html>
```

### Step 3: Verify Links Are Working

After creating these files, verify the links in your `index.html` footer are correct:

**Location:** Lines 824-825

**Should look like:**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-yellow-500 transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-yellow-500 transition-colors duration-300">Terms of Service</a></li>
```

✅ These links are already correct in your HTML!

### File Structure After Creating Pages

Your project folder should now look like this:

```
your-project-folder/
├── index.html          (your main landing page)
├── privacy.html        (newly created)
├── terms.html          (newly created)
└── blog.html           (optional - create if you want)
```

### Customizing the Policy Pages

The templates above are basic starting points. You should customize them with:

1. **Your actual company information**
   - Replace "Lightbox LED" with your company name
   - Replace email addresses with your actual email
   - Update company details and policies

2. **Your specific practices**
   - Describe exactly how you collect and use data
   - List what payment processors you use (Stripe, etc.)
   - Explain your shipping and return policies
   - Add any specific terms for your business

3. **Legal compliance**
   - Consider consulting with a lawyer for your specific jurisdiction
   - Ensure compliance with GDPR (if you serve EU customers)
   - Ensure compliance with CCPA (if you serve California customers)
   - Add any industry-specific requirements

---

## Common Tasks & Troubleshooting

### Task 1: Change the Company Logo/Icon

**Current code:** Lines 85-88

**Current code:**
```html
<a href="#" class="text-2xl font-bold text-gray-900 flex items-center">
    <i class="fas fa-lightbulb text-yellow-500 mr-2"></i>
    <span class="hidden sm:inline">Lightbox LED</span>
    <span class="sm:hidden">LED</span>
</a>
```

**To change the icon:**
1. Visit [Font Awesome Icons](https://fontawesome.com/icons)
2. Search for an icon you like
3. Copy the icon name
4. Replace `fa-lightbulb` with your new icon name

**Example - changing to a camera icon:**
```html
<i class="fas fa-camera text-yellow-500 mr-2"></i>
```

**To change the icon color:**
- Change `text-yellow-500` to another color
- Options: `text-blue-500`, `text-red-500`, `text-green-500`, etc.

### Task 2: Update the Announcement Bar Message

**Current code:** Lines 73-75

**Current code:**
```html
<div class="announcement-bar text-white py-3 px-4 text-center text-sm md:text-base">
    <i class="fas fa-truck mr-2"></i>Fast Worldwide Shipping (5 days delivery) | 100% Satisfaction Guarantee
</div>
```

**To change it:**
1. Replace the text after the icon
2. Keep the `<i>` tag and all classes the same

**Example:**
```html
<div class="announcement-bar text-white py-3 px-4 text-center text-sm md:text-base">
    <i class="fas fa-star mr-2"></i>Free Shipping on Orders Over $100 | 30-Day Money-Back Guarantee
</div>
```

### Task 3: Change Hero Background Image

**Current code:** Line 149

**Current code:**
```html
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=1600&h=900&fit=crop&q=80" 
     alt="Professional photography lighting setup" 
     class="w-full h-full object-cover">
```

**To change the image:**
1. Find a new image URL from:
   - Unsplash (unsplash.com)
   - Pexels (pexels.com)
   - Pixabay (pixabay.com)
   - Your own image (upload to web hosting)

2. Replace the URL in `src="..."`
3. Update the `alt` text to describe your new image

**Example:**
```html
<img src="https://images.unsplash.com/photo-1611532736579-6b16e2b50449?w=1600&h=900&fit=crop&q=80" 
     alt="Professional LED lighting for photography" 
     class="w-full h-full object-cover">
```

### Task 4: Add or Remove a Feature Card

**Current location:** Lines 197-227 (three feature cards)

**To add a new feature card:**

1. Find where the feature cards are (around line 197)
2. Copy one complete feature card (all the HTML)
3. Paste it after the last feature card
4. Update the text, icon, and bullet points

**Example - adding a fourth card:**

**Original (3 cards in a grid):**
```html
<div class="grid grid-cols-1 md:grid-cols-3 gap-8">
    <!-- Card 1 -->
    <div class="feature-card bg-white border border-gray-200 rounded-lg p-8">
        ...
    </div>
    <!-- Card 2 -->
    <div class="feature-card bg-white border border-gray-200 rounded-lg p-8">
        ...
    </div>
    <!-- Card 3 -->
    <div class="feature-card bg-white border border-gray-200 rounded-lg p-8">
        ...
    </div>
</div>
```

**After adding a fourth card:**
```html
<div class="grid grid-cols-1 md:grid-cols-2 gap-8">
    <!-- Change md:grid-cols-3 to md:grid-cols-2 -->
    <!-- Then add your 4 cards -->
</div>
```

**Note:** To maintain responsive design:
- 3 cards: use `md:grid-cols-3`
- 4 cards: use `md:grid-cols-2` or `md:grid-cols-4`
- 2 cards: use `md:grid-cols-2`

### Task 5: Change Button Colors

**Current code example:** Line 162

**Current code:**
```html
<a href="#" class="inline-block px-8 py-4 bg-yellow-500 text-gray-900 font-bold text-lg rounded-lg">
    Get Started Now
</a>
```

**To change button colors:**

| What to Change | Current | Alternative Options |
|---|---|---|
| Background color | `bg-yellow-500` | `bg-blue-600`, `bg-green-600`, `bg-red-600`, `bg-purple-600` |
| Text color | `text-gray-900` | `text-white`, `text-gray-100`, `text-yellow-100` |
| Hover effect text | (add to classes) | Add `hover:bg-yellow-600` to darken on hover |

**Example - blue button with white text:**
```html
<a href="#" class="inline-block px-8 py-4 bg-blue-600 text-white font-bold text-lg rounded-lg hover:bg-blue-700">
    Get Started Now
</a>
```

### Task 6: Make Text Responsive (Mobile vs Desktop)

**Understanding responsive text:**

```html
<h1 class="text-4xl md:text-6xl">Heading</h1>
```

- `text-4xl` = size on mobile/small screens
- `md:text-6xl` = size on medium screens and larger

**Common responsive patterns:**

```html
<!-- Small heading (mobile: 2xl, desktop: 3xl) -->
<h3 class="text-2xl md:text-3xl font-bold">Subheading</h3>

<!-- Large heading (mobile: 3xl, desktop: 5xl) -->
<h1 class="text-3xl md:text-5xl font-bold">Main Heading</h1>

<!-- Text (mobile: base, desktop: lg) -->
<p class="text-base md:text-lg text-gray-700">Body text</p>
```

### Task 7: Troubleshooting Common Issues

#### Issue: Links Don't Work

**Symptom:** Clicking a link does nothing

**Solution:**
1. Check the `href` attribute has a valid URL
2. For internal links (same page), make sure the ID matches
3. For external links, ensure URL starts with `https://`

**Example - fixing a broken link:**
```html
<!-- Broken -->
<a href="#">Click here</a>

<!-- Fixed - internal link -->
<a href="#features">Click here</a>

<!-- Fixed - external link -->
<a href="https://example.com">Click here</a>
```

#### Issue: Text Overlaps on Mobile

**Symptom:** Text is too large or overlaps on phone screens

**Solution:**
1. Add responsive text sizing
2. Reduce padding on mobile

**Example - fixing overlapping text:**
```html
<!-- Before (too large on mobile) -->
<h1 class="text-6xl font-bold">Heading</h1>

<!-- After (responsive) -->
<h1 class="text-3xl md:text-6xl font-bold">Heading</h1>
```

#### Issue: Images Don't Show

**Symptom:** Image placeholder or broken image icon appears

**Solution:**
1. Check the image URL is correct
2. Ensure the URL is publicly accessible
3. For local images, use the correct file path

**Example - fixing image URLs:**
```html
<!-- Broken - URL doesn't exist -->
<img src="https://example.com/wrong-image.jpg">

<!-- Fixed - valid Unsplash URL -->
<img src="https://images.unsplash.com/photo-1504093376055-b3094b674dcb?w=800&h=600&fit=crop&q=80">

<!-- Fixed - local image in same folder -->
<img src="images/my-photo.jpg">
```

#### Issue: Accordion Doesn't Open/Close

**Symptom:** FAQ items don't expand when clicked

**Solution:**
1. Check that JavaScript isn't broken
2. Ensure the accordion button has `onclick="toggleAccordion(this)"`
3. Verify the HTML structure is intact

**Example - correct accordion structure:**
```html
<button class="accordion-button" onclick="toggleAccordion(this)">
    <span>Question text</span>
    <i class="fas fa-chevron-down"></i>
</button>
<div class="accordion-content">
    <div class="p-6">
        Answer text here
    </div>
</div>
```

#### Issue: Mobile Menu Doesn't Open

**Symptom:** Hamburger menu button doesn't show mobile menu

**Solution:**
1. Check that the button ID is `mobile-menu-toggle`
2. Verify the menu ID is `mobile-menu`
3. Ensure JavaScript is not blocked

**Correct code:**
```html
<button id="mobile-menu-toggle">
    <i class="fas fa-bars"></i>
</button>
<div id="mobile-menu" class="hidden">
    <!-- Menu items -->
</div>
```

---

## Best Practices

### 1. Always Test Changes

After making any changes:
- **Desktop:** Open in browser and check layout
- **Mobile:** Use browser's mobile view (F12 key, then click mobile icon)
- **Links:** Click every link to ensure it works
- **Forms:** Test any interactive elements

### 2. Keep Backups

Before making major changes:
1. Save a copy of your original `index.html`
2. Name it `index-backup.html`
3. If something breaks, you can restore the original

### 3. Use Consistent Styling

When making changes:
- Keep the same color scheme (yellow for CTAs, gray for text)
- Use the same font sizes for similar elements
- Maintain consistent spacing throughout
- Keep responsive design patterns (mobile first, then `md:` for desktop)

### 4. Update All Similar Elements

When changing something:
- **Buttons:** Update all buttons the same way
- **Links:** Use consistent link colors and hover effects
- **Headings:** Keep heading sizes consistent
- **Spacing:** Use the same spacing patterns

**Example - if you change button color from yellow to blue:**
- Update ALL "Buy Now" buttons
- Update ALL "Get Started" buttons
- Update ALL CTA buttons
- Keep them all the same color

### 5. Optimize Images

For better performance:
- Use images that are 1600x900px or smaller
- Use JPEG format for photos
- Use PNG for graphics with transparency
- Compress images before uploading
- Always include descriptive `alt` text

### 6. Keep SEO in Mind

For search engine optimization:
- Use descriptive page titles (already done: "Lightbox LED Photography Kits - Professional Lighting Solutions")
- Write meaningful meta descriptions (already done in `<head>`)
- Use heading hierarchy (h1 > h2 > h3)
- Include descriptive alt text for images
- Use relevant keywords naturally in content

### 7. Accessibility Best Practices

Make your site usable for everyone:
- Always include `alt` text for images
- Use sufficient color contrast (dark text on light background)
- Make buttons large enough to click easily
- Use descriptive link text (not "click here")
- Test with keyboard navigation

### 8. Mobile-First Approach

When designing or modifying:
1. Start with mobile/small screen version
2. Add `md:`, `lg:`, etc. for larger screens
3. Never remove mobile styles when adding desktop styles

**Example - correct approach:**
```html
<!-- Good - mobile first, then desktop -->
<h1 class="text-2xl md:text-4xl">Heading</h1>

<!-- Bad - only desktop size, breaks on mobile -->
<h1 class="text-4xl">Heading</h1>
```

### 9. Documentation

Keep track of your changes:
- Note when you update links or content
- Document any customizations you make
- Keep a change log (optional but helpful)
- Save important information (Stripe links, email addresses, etc.)

**Example change log:**
```
Date: January 15, 2024
- Updated Stripe checkout link in 7 locations
- Changed hero headline to "Professional Photography Lighting Solutions"
- Updated company email to support@lightboxled.com
- Created privacy.html and terms.html pages
```

### 10. Security Practices

Protect your website:
- Never share your Stripe checkout link publicly in code comments
- Keep payment information secure (use Stripe, not custom payment systems)
- Regularly backup your website files
- Keep software and plugins updated
- Use HTTPS for your website (secure connection)

---

## Quick Reference Guide

### File Structure
```
project-folder/
├── index.html (main landing page)
├── privacy.html (legal page)
├── terms.html (legal page)
├── blog.html (optional blog page)
└── images/ (optional image folder)
```

### Key Sections to Edit

| Section | Lines | What to Change |
|---------|-------|---|
| Announcement Bar | 73-75 | Shipping/guarantee message |
| Logo | 85-88 | Company name and icon |
| Navigation Links | 99-105 | Menu links (if adding new sections) |
| Hero Headline | 155-157 | Main headline text |
| Hero Subtitle | 158-160 | Subheading text |
| Feature Cards | 197-227 | Feature titles and descriptions |
| Testimonials | 431-477 | Customer reviews |
| FAQ | 551-619 | Questions and answers |
| Contact Email | 701 | Your email address |
| Social Media | 778-791 | Your social profiles |
| Footer Links | 783-836 | Footer navigation |

### Common CSS Color Classes

```
Text Colors:
text-white, text-gray-900, text-gray-700, text-gray-600, text-yellow-500

Background Colors:
bg-white, bg-gray-50, bg-gray-900, bg-yellow-500

Border Colors:
border-gray-200, border-white
```

### Common Tailwind Spacing

```
Padding: p-4, p-6, p-8, p-12
Margin Bottom: mb-3, mb-4, mb-6, mb-8, mb-12
Margin Top: mt-1, mt-4, mt-6
Horizontal Padding: px-4, px-6, px-8
Vertical Padding: py-2, py-3, py-4, py-6
```

---

## Support & Resources

### Where to Find Help

**For HTML/CSS Questions:**
- [MDN Web Docs](https://developer.mozilla.org/) - Comprehensive HTML/CSS documentation
- [W3Schools](https://www.w3schools.com/) - Interactive tutorials
- [CSS-Tricks](https://css-tricks.com/) - CSS tips and tricks

**For Tailwind CSS:**
- [Tailwind CSS Documentation](https://tailwindcss.com/docs) - Official docs
- [Tailwind CSS Playground](https://play.tailwindcss.com/) - Test code online

**For Icons:**
- [Font Awesome Icons](https://fontawesome.com/icons) - Browse all available icons
- [Font Awesome Docs](https://fontawesome.com/docs) - How to use icons

**For Images:**
- [Unsplash](https://unsplash.com/) - Free high-quality images
- [Pexels](https://www.pexels.com/) - Free stock photos
- [Pixabay](https://pixabay.com/) - Free images and videos

**For Code Validation:**
- [W3C HTML Validator](https://validator.w3.org/) - Check your HTML is valid
- [CSS Validator](https://jigsaw.w3.org/css-validator/) - Check your CSS

---

## Final Checklist

Before launching your updated website:

- [ ] All links work correctly (test each one)
- [ ] Email addresses are updated
- [ ] Stripe checkout link is correct
- [ ] Social media links are updated
- [ ] Privacy policy page is created and linked
- [ ] Terms of service page is created and linked
- [ ] Site looks good on mobile (use browser mobile view)
- [ ] All images load correctly
- [ ] Accordion/FAQ items work
- [ ] Mobile menu opens and closes
- [ ] Contact information is accurate
- [ ] Company name and branding are consistent
- [ ] No spelling or grammar errors
- [ ] All buttons have working links
- [ ] Footer information is current

---

## Conclusion

You now have a comprehensive guide to maintain and customize your Lightbox LED Photography landing page. Remember:

1. **Always test changes** before considering them final
2. **Keep backups** of working versions
3. **Follow the existing patterns** for consistency
4. **Keep responsive design** in mind (mobile + desktop)
5. **Update all similar elements** together

If you encounter issues not covered in this guide, refer to the resources section or consult with a web developer. Good luck with your landing page!