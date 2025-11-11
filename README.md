# SOMDA Landing Page - Maintenance & Customization Guide

Welcome to the comprehensive maintenance guide for the SOMDA landing page. This document provides clear, step-by-step instructions for updating content, fixing links, and customizing your website. Whether you're new to web development or just need a refresher, this guide will walk you through every process.

---

## Table of Contents

1. [Quick Start Overview](#quick-start-overview)
2. [Section 1: Updating Text and Tailwind CSS Classes](#section-1-updating-text-and-tailwind-css-classes)
3. [Section 2: Fixing Broken Links](#section-2-fixing-broken-links)
4. [Section 3: Linking Privacy and Terms Pages](#section-3-linking-privacy-and-terms-pages)
5. [Troubleshooting Guide](#troubleshooting-guide)
6. [Best Practices](#best-practices)

---

## Quick Start Overview

### What You Need to Know Before Starting

**File Structure:**
Your website consists of these files:
- `index.html` - The main landing page (the file you have)
- `privacy.html` - Privacy policy page (you'll create this)
- `terms.html` - Terms of service page (you'll create this)
- `blog.html` - Blog page (referenced but optional)

**How to Edit:**
1. Right-click on the `index.html` file
2. Select "Open with" and choose a text editor (Notepad, VS Code, Sublime Text, etc.)
3. Make your changes
4. Save the file (Ctrl+S or Cmd+S)
5. Refresh your browser to see changes

**Key Concepts:**
- **HTML Tags**: Text containers like `<h1>`, `<p>`, `<a>` that tell the browser what type of content they hold
- **Tailwind CSS Classes**: Pre-made styling instructions written in the `class=""` attribute
- **href Attribute**: The link destination in `<a>` tags (like `href="page.html"`)

---

## Section 1: Updating Text and Tailwind CSS Classes

### 1.1 Understanding the Page Structure

Your landing page is organized into clear sections. Here's what each section does:

| Section | Location | Purpose |
|---------|----------|---------|
| **Header & Navigation** | Top of page | Logo, menu links, mobile menu |
| **Hero Section** | Below header | Main headline, call-to-action buttons |
| **Features Section** | Middle | Three service cards |
| **Benefits Section** | Middle | Four benefit items with checkmarks |
| **Testimonials Section** | Lower middle | Client reviews with star ratings |
| **FAQ Section** | Lower | Expandable questions and answers |
| **Footer** | Bottom | Contact info, links, social media |

### 1.2 Updating Headline and Hero Text

**Location:** Lines 70-95 in your HTML file

**Current Text:**
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 leading-tight tracking-tight">
    We Are Family Advocates for <span class="text-primary">Change</span>
</h1>
```

**How to Change It:**

1. Find the `<h1>` tag in the Hero Section
2. Replace "We Are Family Advocates for Change" with your text
3. The `<span class="text-primary">Change</span>` makes the last word purple—keep this structure if you want colored text

**Example - Changing to Different Text:**
```html
<!-- BEFORE -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 leading-tight tracking-tight">
    We Are Family Advocates for <span class="text-primary">Change</span>
</h1>

<!-- AFTER - Your new headline -->
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold text-gray-900 leading-tight tracking-tight">
    Your Legal Partner for <span class="text-primary">Justice</span>
</h1>
```

**Understanding the Classes:**
- `text-5xl md:text-6xl lg:text-7xl` - Text size changes based on screen size (5xl on mobile, 6xl on tablets, 7xl on desktops)
- `font-bold` - Makes text bold
- `text-gray-900` - Dark gray color
- `text-primary` - Uses the purple color defined in the style section

### 1.3 Updating the Tagline

**Location:** Lines 96-99

**Current Text:**
```html
<p class="text-xl md:text-2xl text-gray-700 font-medium leading-relaxed">
    Voice for the Voiceless — We Fight GBV & Family Conflict
</p>
```

**How to Change It:**

Simply replace the text between the `<p>` and `</p>` tags:

```html
<!-- BEFORE -->
<p class="text-xl md:text-2xl text-gray-700 font-medium leading-relaxed">
    Voice for the Voiceless — We Fight GBV & Family Conflict
</p>

<!-- AFTER -->
<p class="text-xl md:text-2xl text-gray-700 font-medium leading-relaxed">
    Your trusted legal team for family matters
</p>
```

### 1.4 Updating Feature Cards

**Location:** Lines 153-205

Your page has three feature cards. Here's how to update each one:

**Finding the Cards:**
Look for sections that start with `<!-- Feature Card 1 -->`, `<!-- Feature Card 2 -->`, `<!-- Feature Card 3 -->`

**Card Structure:**
```html
<div class="feature-card card-hover bg-white border-2 border-gray-100 rounded-2xl p-8 shadow-lg">
    <!-- Icon SVG goes here -->
    <h3 class="text-2xl font-bold text-gray-900 mb-3">TITLE HERE</h3>
    <p class="text-gray-600 leading-relaxed">
        DESCRIPTION HERE
    </p>
</div>
```

**Example - Updating Feature Card 1:**

**Current:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">Experienced Attorneys</h3>
<p class="text-gray-600 leading-relaxed">
    Our team of highly qualified legal professionals brings decades of combined experience...
</p>
```

**Updated:**
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">Expert Legal Team</h3>
<p class="text-gray-600 leading-relaxed">
    Our specialized attorneys have over 50 years of combined experience in family law and advocacy.
</p>
```

**Changing Card Icons:**

Each card has an SVG icon. To change the icon, replace the entire `<svg>` block. Here are common icon options:

- **Shield Icon** (for protection): Replace the path with `d="M12 22s8-4 8-10V5l-8-3-8 3v7c0 6 8 10 8 10z"`
- **Heart Icon** (for care): Replace with `d="M20.84 4.61a5.5 5.5 0 0 0-7.78 0L12 5.67l-1.06-1.06a5.5 5.5 0 0 0-7.78 7.78l1.06 1.06L12 21.23l7.78-7.78 1.06-1.06a5.5 5.5 0 0 0 0-7.78z"`
- **Star Icon** (for excellence): Replace with `d="M13 2l3.29 6.71A1 1 0 0 0 17.29 9h7.41l-6 4.29a1 1 0 0 0-.37 1.15l2.3 7.37L13 17.77a1 1 0 0 0-1.63 0l-5.62 4.04 2.3-7.37a1 1 0 0 0-.37-1.15l-6-4.29h7.41a1 1 0 0 0 .99-.71L13 2z"`

### 1.5 Updating Benefits Section

**Location:** Lines 230-290

The benefits section has four items with checkmarks. Here's how to update them:

**Current Structure:**
```html
<div class="flex gap-6">
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-12 w-12 rounded-xl gradient-primary">
            <!-- Checkmark icon here -->
        </div>
    </div>
    <div>
        <h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-2">BENEFIT TITLE</h3>
        <p class="text-gray-700 leading-relaxed">
            BENEFIT DESCRIPTION
        </p>
    </div>
</div>
```

**Example - Updating Benefit 1:**

**Current:**
```html
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-2">Expert Legal Representation</h3>
<p class="text-gray-700 leading-relaxed">
    Our attorneys have successfully handled hundreds of cases...
</p>
```

**Updated:**
```html
<h3 class="text-xl md:text-2xl font-bold text-gray-900 mb-2">Award-Winning Attorneys</h3>
<p class="text-gray-700 leading-relaxed">
    Our team has won over 200 cases and earned recognition for excellence in family law.
</p>
```

### 1.6 Updating Testimonials

**Location:** Lines 445-560

Each testimonial card contains:
- Star ratings
- Client quote
- Client name
- Client title

**Current Structure:**
```html
<div class="card-hover bg-white border-2 border-gray-100 rounded-2xl p-8 shadow-lg">
    <!-- Star ratings here -->
    <p class="text-gray-700 leading-relaxed mb-6">
        "CLIENT QUOTE HERE"
    </p>
    <div>
        <p class="font-bold text-gray-900">CLIENT NAME</p>
        <p class="text-gray-600 text-sm">CLIENT TITLE/DESCRIPTION</p>
    </div>
</div>
```

**Example - Updating Testimonial 1:**

**Current:**
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "SOMDA's team changed my life. When I had nowhere to turn..."
</p>
<div>
    <p class="font-bold text-gray-900">Sarah Mitchell</p>
    <p class="text-gray-600 text-sm">Domestic Violence Survivor</p>
</div>
```

**Updated:**
```html
<p class="text-gray-700 leading-relaxed mb-6">
    "The SOMDA team provided compassionate and professional support when I needed it most. They fought for my rights and helped me rebuild my life with dignity and hope."
</p>
<div>
    <p class="font-bold text-gray-900">Maria Rodriguez</p>
    <p class="text-gray-600 text-sm">Family Law Client</p>
</div>
```

**Adjusting Star Ratings:**

Each testimonial has 5 star SVG elements. To show fewer stars, delete the extra `<svg>` lines:

```html
<!-- CURRENT - 5 stars -->
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>

<!-- UPDATED - 4 stars (delete the last one) -->
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
<svg class="w-5 h-5 star-rating" fill="currentColor" viewBox="0 0 20 20">...</svg>
```

### 1.7 Updating FAQ Questions and Answers

**Location:** Lines 595-700

Each FAQ item has this structure:

```html
<div class="faq-item bg-white rounded-xl border-2 border-gray-100 overflow-hidden shadow-lg hover-scale">
    <button class="faq-question w-full px-6 md:px-8 py-6 md:py-8 flex items-center justify-between cursor-pointer hover:bg-gray-50 transition-colors duration-300">
        <h3 class="text-lg md:text-xl font-bold text-gray-900 text-left">QUESTION HERE?</h3>
        <!-- Icon here -->
    </button>
    <div class="faq-answer hidden border-t border-gray-200 px-6 md:px-8 py-6 md:py-8 bg-gray-50">
        <p class="text-gray-700 leading-relaxed">
            ANSWER HERE
        </p>
    </div>
</div>
```

**Example - Updating FAQ Item 1:**

**Current:**
```html
<h3 class="text-lg md:text-xl font-bold text-gray-900 text-left">What types of cases does SOMDA handle?</h3>
<!-- Answer -->
<p class="text-gray-700 leading-relaxed">
    SOMDA specializes in a comprehensive range of family law...
</p>
```

**Updated:**
```html
<h3 class="text-lg md:text-xl font-bold text-gray-900 text-left">What makes SOMDA different?</h3>
<!-- Answer -->
<p class="text-gray-700 leading-relaxed">
    SOMDA combines legal expertise with compassionate support, offering not just representation but a complete care package including counseling referrals and safety planning.
</p>
```

### 1.8 Updating Footer Text

**Location:** Lines 740-800

**Current Footer Logo/Name Section:**
```html
<div class="flex items-center gap-2 mb-4">
    <div class="w-10 h-10 gradient-primary rounded-lg flex items-center justify-center">
        <span class="text-white font-bold text-lg">S</span>
    </div>
    <span class="text-2xl font-bold">SOMDA</span>
</div>
<p class="text-gray-400 leading-relaxed">
    Family advocates committed to fighting gender-based violence...
</p>
```

**To Update:**
- Change "S" to your organization's first letter
- Change "SOMDA" to your organization name
- Update the description text

**Example:**
```html
<span class="text-white font-bold text-lg">L</span>
<!-- Change S to L -->

<span class="text-2xl font-bold">LegalAid Pro</span>
<!-- Change SOMDA to your name -->

<p class="text-gray-400 leading-relaxed">
    Professional legal services dedicated to protecting families and ensuring justice.
</p>
<!-- Update description -->
```

### 1.9 Understanding and Modifying Tailwind Classes

**What Are Tailwind Classes?**

Tailwind CSS is a system of pre-made style instructions. Instead of writing CSS code, you add class names to HTML elements. Here are the most common ones you'll encounter:

| Class | What It Does | Examples |
|-------|-------------|----------|
| **Text Size** | Controls font size | `text-sm`, `text-lg`, `text-2xl`, `text-5xl` |
| **Text Color** | Changes text color | `text-gray-900`, `text-primary`, `text-white` |
| **Background Color** | Changes background | `bg-white`, `bg-secondary`, `bg-gray-50` |
| **Padding** | Inner spacing | `p-4`, `p-8`, `px-6`, `py-4` |
| **Margin** | Outer spacing | `m-4`, `mb-6`, `gap-8` |
| **Border** | Adds borders | `border`, `border-2`, `border-gray-100` |
| **Rounded Corners** | Rounds edges | `rounded-lg`, `rounded-2xl`, `rounded-full` |
| **Font Weight** | Text thickness | `font-medium`, `font-bold`, `font-semibold` |
| **Responsive** | Changes by screen size | `md:text-2xl`, `lg:p-8` |

**Responsive Prefixes Explained:**

Your page uses responsive classes that change based on screen size:

- **No prefix** (e.g., `text-5xl`) = Mobile phones
- **`md:`** (e.g., `md:text-6xl`) = Tablets and larger (medium screens)
- **`lg:`** (e.g., `lg:text-7xl`) = Desktops (large screens)

**Example - Making Text Larger:**

```html
<!-- BEFORE - Smaller on all screens -->
<h2 class="text-2xl md:text-3xl font-bold">Our Services</h2>

<!-- AFTER - Larger on all screens -->
<h2 class="text-3xl md:text-4xl lg:text-5xl font-bold">Our Services</h2>
```

**Example - Adding More Padding:**

```html
<!-- BEFORE - Less padding -->
<div class="p-4 md:p-6">Content</div>

<!-- AFTER - More padding -->
<div class="p-6 md:p-8 lg:p-10">Content</div>
```

**Color Classes Available:**

Your page uses these color classes:
- `text-primary` = Purple (#5B4BFF)
- `text-accent` = Teal/Green (#00E5A8)
- `bg-secondary` = Light purple (#EEF0FF)
- `text-gray-900` = Very dark gray (almost black)
- `text-gray-700` = Medium gray
- `text-gray-600` = Lighter gray
- `text-white` = White
- `text-gray-400` = Light gray (footer text)

### 1.10 Changing Color Scheme

**Location:** Lines 22-28 (in the `<style>` section)

If you want to change the main colors, update these CSS variables:

```html
<style>
    .gradient-primary {
        background: linear-gradient(135deg, #5B4BFF 0%, #00E5A8 100%);
        /* Change #5B4BFF (purple) and #00E5A8 (teal) */
    }
    
    .text-primary {
        color: #5B4BFF;
        /* Change this to your primary color */
    }
    
    .text-accent {
        color: #00E5A8;
        /* Change this to your accent color */
    }
    
    .bg-secondary {
        background-color: #EEF0FF;
        /* Change this to your light background color */
    }
</style>
```

**How to Change Colors:**

1. Find a color you like at [colorpicker.com](https://www.colorpicker.com)
2. Copy the hex code (e.g., `#FF5733`)
3. Replace the hex codes in the style section

**Example - Changing from Purple/Teal to Blue/Orange:**

```html
<!-- BEFORE -->
.gradient-primary {
    background: linear-gradient(135deg, #5B4BFF 0%, #00E5A8 100%);
}
.text-primary {
    color: #5B4BFF;
}
.text-accent {
    color: #00E5A8;
}
.bg-secondary {
    background-color: #EEF0FF;
}

<!-- AFTER -->
.gradient-primary {
    background: linear-gradient(135deg, #1E40AF 0%, #FF8C42 100%);
}
.text-primary {
    color: #1E40AF;
}
.text-accent {
    color: #FF8C42;
}
.bg-secondary {
    background-color: #F0F4FF;
}
```

---

## Section 2: Fixing Broken Links

### 2.1 Understanding Links

A link in HTML looks like this:

```html
<a href="page-to-go-to.html">Click Here</a>
```

The `href` attribute tells the browser where to go when someone clicks the link.

**Types of Links:**
- **Internal links** - Point to pages on your website (e.g., `href="privacy.html"`)
- **External links** - Point to other websites (e.g., `href="https://example.com"`)
- **Anchor links** - Jump to sections on the same page (e.g., `href="#features"`)
- **Email links** - Open email client (e.g., `href="mailto:info@example.com"`)
- **Phone links** - Open phone dialer (e.g., `href="tel:+1234567890"`)

### 2.2 Finding All Links in Your Page

**Navigation Links - Location: Lines 45-52**

```html
<a href="#features" class="...">Features</a>
<a href="#benefits" class="...">Benefits</a>
<a href="#testimonials" class="...">Testimonials</a>
<a href="#faq" class="...">FAQ</a>
<a href="https://somda.co.za/contact/" class="...">Get Started</a>
```

**What These Do:**
- `#features`, `#benefits`, etc. = Jump to those sections on the page
- `https://somda.co.za/contact/` = Goes to external website

### 2.3 Fixing the "Get Started" Button Links

**Current Link:**
```html
<a href="https://somda.co.za/contact/" class="btn-gradient text-white px-8 py-3 rounded-lg font-bold text-base">
    Get Started
</a>
```

**Locations where this appears:**
1. Header navigation (Line 52)
2. Hero section (Line 87)
3. Hero section (Line 91)
4. CTA section (Line 408)
5. Final CTA section (Line 675)

**How to Fix:**

If you want the button to link to a contact form on your site, change it to:

```html
<!-- Option 1: Link to contact section on same page -->
<a href="#contact" class="btn-gradient text-white px-8 py-3 rounded-lg font-bold text-base">
    Get Started
</a>

<!-- Option 2: Link to external contact page -->
<a href="https://yourwebsite.com/contact/" class="btn-gradient text-white px-8 py-3 rounded-lg font-bold text-base">
    Get Started
</a>

<!-- Option 3: Link to email -->
<a href="mailto:info@yourcompany.com" class="btn-gradient text-white px-8 py-3 rounded-lg font-bold text-base">
    Get Started
</a>
```

**Step-by-Step to Update All "Get Started" Links:**

1. Open your HTML file in a text editor
2. Press `Ctrl+H` (or `Cmd+H` on Mac) to open Find & Replace
3. In "Find" box, paste: `https://somda.co.za/contact/`
4. In "Replace" box, paste your new link (e.g., `#contact`)
5. Click "Replace All"
6. Save the file

### 2.4 Fixing Contact Information Links

**Location: Lines 630-660 (Contact Form Section)**

**Current Email Link:**
```html
<a href="mailto:hello@example.com" class="text-blue-600 hover:text-blue-700">
    hello@example.com
</a>
```

**Current Phone Link:**
```html
<a href="tel:+1234567890" class="text-blue-600 hover:text-blue-700">
    +1 (234) 567-890
</a>
```

**How to Update:**

Replace the placeholder email and phone with your actual contact information:

```html
<!-- BEFORE -->
<a href="mailto:hello@example.com">hello@example.com</a>
<a href="tel:+1234567890">+1 (234) 567-890</a>

<!-- AFTER -->
<a href="mailto:info@somda.co.za">info@somda.co.za</a>
<a href="tel:+27123456789">+27 (12) 345-6789</a>
```

**Important Notes:**
- For email: Use `mailto:` prefix
- For phone: Use `tel:` prefix with country code (e.g., +27 for South Africa)
- No spaces in phone numbers with `tel:` links

### 2.5 Fixing Footer Links

**Location: Lines 740-800**

Your footer has several link sections:

**Services Links:**
```html
<li><a href="#features" class="text-gray-400 hover:text-accent transition-colors duration-300">Legal Representation</a></li>
<li><a href="#features" class="text-gray-400 hover:text-accent transition-colors duration-300">Private Investigations</a></li>
<li><a href="#benefits" class="text-gray-400 hover:text-accent transition-colors duration-300">Support Services</a></li>
<li><a href="#faq" class="text-gray-400 hover:text-accent transition-colors duration-300">Crisis Support</a></li>
```

**These are fine** - they link to sections on the current page.

**Resources Links:**
```html
<li><a href="blog.html" class="text-gray-400 hover:text-accent transition-colors duration-300">Blog</a></li>
<li><a href="privacy.html" class="text-gray-400 hover:text-accent transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-accent transition-colors duration-300">Terms of Service</a></li>
<li><a href="#faq" class="text-gray-400 hover:text-accent transition-colors duration-300">FAQ</a></li>
```

**These need pages created** - See Section 3 for creating privacy.html and terms.html

**Contact Links:**
```html
<a href="mailto:info@somda.co.za" class="text-gray-400 hover:text-accent transition-colors duration-300">
    info@somda.co.za
</a>
```

**Update this** to your actual email address.

**Social Media Links:**
```html
<a href="#" class="text-gray-400 hover:text-accent transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

**These currently go nowhere** (`href="#"`). Update them to your social media profiles:

```html
<!-- BEFORE -->
<a href="#" class="text-gray-400 hover:text-accent transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>

<!-- AFTER -->
<a href="https://facebook.com/yourpage" class="text-gray-400 hover:text-accent transition-colors duration-300" aria-label="Facebook">
    <i class="fab fa-facebook-f"></i>
</a>
```

### 2.6 Quick Reference: All Links to Check

Use this checklist to find and fix all links:

**Navigation Bar (Top of page):**
- [ ] Get Started button - Should link to contact form or page
- [ ] Features link - Should jump to #features (should work)
- [ ] Benefits link - Should jump to #benefits (should work)
- [ ] Testimonials link - Should jump to #testimonials (should work)
- [ ] FAQ link - Should jump to #faq (should work)

**Mobile Menu (Mobile devices only):**
- [ ] All same links as navigation bar

**Hero Section:**
- [ ] Schedule Consultation button - Should link to contact page
- [ ] Learn More button - Should jump to #features (should work)

**CTA Section (Middle of page):**
- [ ] Start Your Case Today button - Should link to contact page

**Contact Form Section:**
- [ ] Email link - Update to your email
- [ ] Phone link - Update to your phone number

**Footer:**
- [ ] All Service links - Should jump to sections (should work)
- [ ] Blog link - Create blog.html or remove
- [ ] Privacy Policy link - Create privacy.html
- [ ] Terms of Service link - Create terms.html
- [ ] Email link - Update to your email
- [ ] Social media links - Update to your profiles

---

## Section 3: Linking Privacy and Terms Pages

### 3.1 Understanding What You Need to Create

Your landing page references two pages that don't exist yet:
1. `privacy.html` - Privacy Policy page
2. `terms.html` - Terms of Service page

These are linked in:
- Footer (4 times)
- Footer bottom links (2 times)

**Total: 6 links that need these pages**

### 3.2 Creating the Privacy Policy Page

**Step 1: Create a New File**

1. Open your text editor (same one you use for index.html)
2. Click File → New File
3. Leave it blank
4. Save it as `privacy.html` in the same folder as your `index.html`

**Step 2: Copy the Template**

Here's a complete privacy policy template. Copy and paste this into your new `privacy.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="SOMDA Privacy Policy - How we protect your personal information">
    <meta name="author" content="SOMDA">
    <title>Privacy Policy - SOMDA</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        .text-primary {
            color: #5B4BFF;
        }
        .gradient-primary {
            background: linear-gradient(135deg, #5B4BFF 0%, #00E5A8 100%);
        }
        .sticky-header {
            position: sticky;
            top: 0;
            z-index: 50;
            background: white;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header -->
    <header class="sticky-header">
        <nav class="max-w-7xl mx-auto px-4 md:px-8 py-4 md:py-6 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 gradient-primary rounded-lg flex items-center justify-center">
                    <span class="text-white font-bold text-lg">S</span>
                </div>
                <span class="text-2xl font-bold text-primary hidden sm:inline">SOMDA</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-primary font-medium transition-colors duration-300">← Back to Home</a>
        </nav>
    </header>

    <!-- Privacy Policy Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 md:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Privacy Policy</h1>
            <p class="text-gray-600 mb-8">Last Updated: January 2025</p>

            <div class="space-y-8 text-gray-700 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Introduction</h2>
                    <p>
                        SOMDA ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and otherwise process personal information in connection with our websites, mobile applications, and services (collectively, the "Services").
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Information We Collect</h2>
                    <p class="mb-4">We collect information you provide directly, such as:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Contact information (name, email, phone number)</li>
                        <li>Case information and legal history</li>
                        <li>Payment information for services</li>
                        <li>Communication preferences</li>
                        <li>Information you provide through contact forms</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. How We Use Your Information</h2>
                    <p class="mb-4">We use collected information to:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Provide legal services and support</li>
                        <li>Respond to your inquiries</li>
                        <li>Process payments</li>
                        <li>Improve our services</li>
                        <li>Comply with legal obligations</li>
                        <li>Protect your rights and safety</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Confidentiality and Attorney-Client Privilege</h2>
                    <p>
                        All communications between you and our attorneys are protected by attorney-client privilege and confidentiality laws. We maintain strict security measures to protect sensitive information related to your case.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Information Sharing</h2>
                    <p>
                        We do not share your personal information with third parties except: (a) as necessary to provide our services, (b) with your consent, (c) to comply with legal obligations, or (d) to protect your safety and rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Data Security</h2>
                    <p>
                        We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Your Rights</h2>
                    <p class="mb-4">You have the right to:</p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Access your personal information</li>
                        <li>Request correction of inaccurate information</li>
                        <li>Request deletion of your information</li>
                        <li>Opt-out of marketing communications</li>
                        <li>Data portability</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Contact Us</h2>
                    <p>
                        If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                    </p>
                    <p class="mt-4">
                        Email: <a href="mailto:info@somda.co.za" class="text-primary hover:underline">info@somda.co.za</a><br>
                        Phone: <a href="tel:+27123456789" class="text-primary hover:underline">+27 (12) 345-6789</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 md:px-8">
            <div class="text-center mb-8">
                <p class="text-gray-400">
                    &copy; 2025 SOMDA. All rights reserved.
                </p>
            </div>
            <div class="text-center">
                <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">← Back to Home</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the Privacy Policy**

Replace the placeholder information with your actual details:

1. Find `info@somda.co.za` and replace with your email
2. Find `+27123456789` and replace with your phone
3. Update the "Last Updated" date
4. Modify any sections that don't apply to your business

### 3.3 Creating the Terms of Service Page

**Step 1: Create a New File**

1. Open your text editor
2. Click File → New File
3. Save it as `terms.html` in the same folder as your `index.html`

**Step 2: Copy the Template**

Here's a complete terms of service template. Copy and paste this into your new `terms.html` file:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="SOMDA Terms of Service">
    <meta name="author" content="SOMDA">
    <title>Terms of Service - SOMDA</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        .text-primary {
            color: #5B4BFF;
        }
        .gradient-primary {
            background: linear-gradient(135deg, #5B4BFF 0%, #00E5A8 100%);
        }
        .sticky-header {
            position: sticky;
            top: 0;
            z-index: 50;
            background: white;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header -->
    <header class="sticky-header">
        <nav class="max-w-7xl mx-auto px-4 md:px-8 py-4 md:py-6 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 gradient-primary rounded-lg flex items-center justify-center">
                    <span class="text-white font-bold text-lg">S</span>
                </div>
                <span class="text-2xl font-bold text-primary hidden sm:inline">SOMDA</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-primary font-medium transition-colors duration-300">← Back to Home</a>
        </nav>
    </header>

    <!-- Terms of Service Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 md:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Terms of Service</h1>
            <p class="text-gray-600 mb-8">Last Updated: January 2025</p>

            <div class="space-y-8 text-gray-700 leading-relaxed">
                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">1. Acceptance of Terms</h2>
                    <p>
                        By accessing and using the SOMDA website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">2. Use License</h2>
                    <p class="mb-4">
                        Permission is granted to temporarily download one copy of the materials (information or software) on SOMDA's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                    </p>
                    <ul class="list-disc list-inside space-y-2 ml-4">
                        <li>Modify or copy the materials</li>
                        <li>Use the materials for any commercial purpose or for any public display</li>
                        <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                        <li>Remove any copyright or other proprietary notations from the materials</li>
                        <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    </ul>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">3. Disclaimer</h2>
                    <p>
                        The materials on SOMDA's website are provided on an 'as is' basis. SOMDA makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">4. Limitations</h2>
                    <p>
                        In no event shall SOMDA or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on SOMDA's website, even if SOMDA or an authorized representative has been notified orally or in writing of the possibility of such damage.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">5. Accuracy of Materials</h2>
                    <p>
                        The materials appearing on SOMDA's website could include technical, typographical, or photographic errors. SOMDA does not warrant that any of the materials on its website are accurate, complete, or current. SOMDA may make changes to the materials contained on its website at any time without notice.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">6. Links</h2>
                    <p>
                        SOMDA has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by SOMDA of the site. Use of any such linked website is at the user's own risk.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">7. Modifications</h2>
                    <p>
                        SOMDA may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">8. Legal Services Disclaimer</h2>
                    <p>
                        Nothing on this website constitutes legal advice. No attorney-client relationship is formed by viewing this website. If you need legal advice, please contact our office directly to schedule a consultation with one of our attorneys.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">9. Governing Law</h2>
                    <p>
                        These terms and conditions are governed by and construed in accordance with the laws of South Africa, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                    </p>
                </section>

                <section>
                    <h2 class="text-2xl font-bold text-gray-900 mb-4">10. Contact Information</h2>
                    <p>
                        If you have any questions about these Terms of Service, please contact us at:
                    </p>
                    <p class="mt-4">
                        Email: <a href="mailto:info@somda.co.za" class="text-primary hover:underline">info@somda.co.za</a><br>
                        Phone: <a href="tel:+27123456789" class="text-primary hover:underline">+27 (12) 345-6789</a>
                    </p>
                </section>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 md:px-8">
            <div class="text-center mb-8">
                <p class="text-gray-400">
                    &copy; 2025 SOMDA. All rights reserved.
                </p>
            </div>
            <div class="text-center">
                <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">← Back to Home</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

**Step 3: Customize the Terms of Service**

Replace the placeholder information:

1. Find `info@somda.co.za` and replace with your email
2. Find `+27123456789` and replace with your phone
3. Update the "Last Updated" date
4. Change "South Africa" to your country if needed
5. Modify any sections specific to your business

### 3.4 Creating a Blog Page (Optional)

Your footer also links to `blog.html`. If you want to create this page, follow the same process:

**Step 1: Create the file**
- Create a new file and save it as `blog.html`

**Step 2: Use this template:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="SOMDA Blog - Legal Insights and Updates">
    <meta name="author" content="SOMDA">
    <title>Blog - SOMDA</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    <style>
        * {
            font-family: 'Inter', sans-serif;
        }
        .text-primary {
            color: #5B4BFF;
        }
        .gradient-primary {
            background: linear-gradient(135deg, #5B4BFF 0%, #00E5A8 100%);
        }
        .sticky-header {
            position: sticky;
            top: 0;
            z-index: 50;
            background: white;
            box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header -->
    <header class="sticky-header">
        <nav class="max-w-7xl mx-auto px-4 md:px-8 py-4 md:py-6 flex justify-between items-center">
            <div class="flex items-center gap-2">
                <div class="w-10 h-10 gradient-primary rounded-lg flex items-center justify-center">
                    <span class="text-white font-bold text-lg">S</span>
                </div>
                <span class="text-2xl font-bold text-primary hidden sm:inline">SOMDA</span>
            </div>
            <a href="index.html" class="text-gray-700 hover:text-primary font-medium transition-colors duration-300">← Back to Home</a>
        </nav>
    </header>

    <!-- Blog Content -->
    <section class="py-16 md:py-24 bg-white">
        <div class="max-w-4xl mx-auto px-4 md:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4">Our Blog</h1>
            <p class="text-gray-600 mb-12">Legal insights, updates, and resources for families facing conflict and violence</p>

            <div class="space-y-12">
                <!-- Blog Post 1 -->
                <article class="border-b border-gray-200 pb-12">
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">Understanding Your Rights in Family Law</h2>
                    <p class="text-gray-600 mb-4">Published: January 15, 2025</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Family law can be complex and overwhelming. In this article, we break down the fundamental rights you have during family disputes, from custody arrangements to property division...
                    </p>
                    <a href="#" class="text-primary hover:underline font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 2 -->
                <article class="border-b border-gray-200 pb-12">
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">Protecting Yourself from Gender-Based Violence</h2>
                    <p class="text-gray-600 mb-4">Published: January 10, 2025</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        If you're experiencing gender-based violence, you're not alone. This guide provides practical steps to protect yourself and access the support you deserve...
                    </p>
                    <a href="#" class="text-primary hover:underline font-semibold">Read More →</a>
                </article>

                <!-- Blog Post 3 -->
                <article>
                    <h2 class="text-2xl font-bold text-gray-900 mb-2">Navigating Custody Battles: What You Need to Know</h2>
                    <p class="text-gray-600 mb-4">Published: January 5, 2025</p>
                    <p class="text-gray-700 leading-relaxed mb-4">
                        Custody disputes are emotionally challenging. Our team explains the legal process and shares strategies to help you advocate for your children's best interests...
                    </p>
                    <a href="#" class="text-primary hover:underline font-semibold">Read More →</a>
                </article>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-white py-16 md:py-20">
        <div class="max-w-7xl mx-auto px-4 md:px-8">
            <div class="text-center mb-8">
                <p class="text-gray-400">
                    &copy; 2025 SOMDA. All rights reserved.
                </p>
            </div>
            <div class="text-center">
                <a href="index.html" class="text-gray-400 hover:text-white transition-colors duration-300">← Back to Home</a>
            </div>
        </div>
    </footer>
</body>
</html>
```

### 3.5 Verifying All Links Work

**After creating privacy.html, terms.html, and blog.html:**

1. Open `index.html` in your browser
2. Click each footer link to verify they work:
   - Privacy Policy → Should open privacy.html
   - Terms of Service → Should open terms.html
   - Blog → Should open blog.html
3. Each of those pages should have a "Back to Home" link that returns to index.html

**If a link doesn't work:**
- Make sure the file names are spelled correctly (lowercase, with `.html` extension)
- Make sure all files are in the same folder
- Clear your browser cache (Ctrl+Shift+Delete) and refresh

### 3.6 Updating Contact Information in All Pages

You need to update the email and phone in three places:

**1. In index.html (main page):**
- Line 52: Get Started button link
- Line 87, 91: Hero section buttons
- Line 408: CTA section button
- Line 675: Final CTA button
- Line 630-660: Contact form section (email and phone)
- Line 775: Footer email link

**2. In privacy.html:**
- Line 117: Email link
- Line 117: Phone link

**3. In terms.html:**
- Line 123: Email link
- Line 123: Phone link

**Quick Update Method:**

Use Find & Replace in your text editor for all files:

1. Open each file
2. Press Ctrl+H (or Cmd+H)
3. Find: `info@somda.co.za`
4. Replace with: your actual email
5. Find: `+27123456789`
6. Replace with: your actual phone
7. Save

---

## Troubleshooting Guide

### Problem: Links Don't Work

**Symptom:** Clicking a link does nothing or shows "Page not found"

**Solutions:**

1. **Check the file name:**
   ```
   ❌ Wrong: href="Privacy.html" (capital P)
   ✅ Correct: href="privacy.html" (lowercase)
   ```

2. **Check the file exists:**
   - Make sure `privacy.html`, `terms.html`, and `blog.html` are in the same folder as `index.html`
   - If they're in a subfolder, update the link: `href="pages/privacy.html"`

3. **Check for typos:**
   ```
   ❌ Wrong: href="privacyy.html" (extra y)
   ✅ Correct: href="privacy.html"
   ```

4. **Check anchor links (jump links):**
   ```
   ❌ Wrong: href="#feature" (doesn't match id)
   ✅ Correct: href="#features" (matches the section id)
   ```

### Problem: Text Changes Don't Show Up

**Symptom:** You edited the HTML but the page still shows old text

**Solutions:**

1. **Save the file:**
   - Press Ctrl+S (or Cmd+S) after making changes
   - Check the title bar—it shouldn't have an asterisk (*)

2. **Hard refresh your browser:**
   - Press Ctrl+Shift+R (or Cmd+Shift+R on Mac)
   - This clears cached files and forces the browser to load fresh

3. **Check you edited the right file:**
   - Make sure you're editing `index.html`, not a backup copy
   - Check the file path in your editor

### Problem: Styling Looks Wrong

**Symptom:** Text is wrong size, colors are wrong, or layout is broken

**Solutions:**

1. **Check you didn't break the HTML structure:**
   ```
   ❌ Wrong: <h1 class="text-5xl">Headline</h1> (missing closing tag)
   ✅ Correct: <h1 class="text-5xl">Headline</h1>
   ```

2. **Check for missing class names:**
   ```
   ❌ Wrong: <h1 class="text-5xl font-bold">Headline</h1 (missing >)
   ✅ Correct: <h1 class="text-5xl font-bold">Headline</h1>
   ```

3. **Check Tailwind CDN is loading:**
   - Open your browser's developer tools (F12)
   - Go to Console tab
   - Look for any red errors about Tailwind or scripts

### Problem: Mobile Menu Doesn't Work

**Symptom:** Hamburger menu icon appears but clicking it doesn't open the menu

**Solutions:**

1. **Check the JavaScript is not broken:**
   - Open developer tools (F12)
   - Go to Console tab
   - Look for red errors
   - If you see errors, you may have accidentally deleted or modified JavaScript code

2. **Check the mobile menu button HTML is intact:**
   - Search for `mobile-menu-button` in your HTML
   - Make sure all the code is there and not accidentally deleted

3. **Clear cache and refresh:**
   - Press Ctrl+Shift+R to do a hard refresh

### Problem: Form Doesn't Submit

**Symptom:** Clicking "Send Message" in the contact form doesn't work

**Solutions:**

1. **Check the Web3Forms access key:**
   - Look for this line in the HTML: `<input type="hidden" name="access_key" value="3bb39263-2490-491b-89f8-213fa513edae">`
   - This is a unique key provided by Web3Forms
   - If you need a new form, get a new key from [web3forms.com](https://web3forms.com)

2. **Check all required fields are filled:**
   - Name field has `required`
   - Email field has `required`
   - Message field has `required`
   - User must fill all three

3. **Check browser console for errors:**
   - Press F12 to open developer tools
   - Go to Console tab
   - Submit the form and look for red errors

### Problem: Colors Don't Match Brand

**Symptom:** The purple and teal colors don't match your brand

**Solutions:**

1. **Find your brand colors:**
   - Use [colorpicker.com](https://www.colorpicker.com) to find hex codes
   - For example: `#FF5733` is a red color

2. **Update the style section:**
   ```html
   <style>
       .gradient-primary {
           background: linear-gradient(135deg, #YOUR-COLOR-1 0%, #YOUR-COLOR-2 100%);
       }
       .text-primary {
           color: #YOUR-COLOR-1;
       }
       .text-accent {
           color: #YOUR-COLOR-2;
       }
       .bg-secondary {
           background-color: #LIGHT-VERSION-OF-COLOR-1;
       }
   </style>
   ```

3. **Example - Changing to Blue/Orange:**
   ```html
   <style>
       .gradient-primary {
           background: linear-gradient(135deg, #1E40AF 0%, #FF8C42 100%);
       }
       .text-primary {
           color: #1E40AF;
       }
       .text-accent {
           color: #FF8C42;
       }
       .bg-secondary {
           background-color: #F0F4FF;
       }
   </style>
   ```

### Problem: Text is Too Small or Too Large

**Symptom:** Headline or body text isn't the right size

**Solutions:**

1. **Understand responsive text sizes:**
   ```html
   <!-- Mobile: text-2xl, Tablet: text-3xl, Desktop: text-4xl -->
   <h2 class="text-2xl md:text-3xl lg:text-4xl">Headline</h2>
   ```

2. **Make text larger:**
   ```html
   <!-- BEFORE - Smaller -->
   <h2 class="text-2xl md:text-3xl lg:text-4xl">Headline</h2>
   
   <!-- AFTER - Larger -->
   <h2 class="text-3xl md:text-4xl lg:text-5xl">Headline</h2>
   ```

3. **Text size scale (from smallest to largest):**
   - `text-xs`, `text-sm`, `text-base`, `text-lg`, `text-xl`
   - `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`, `text-7xl`

### Problem: Spacing Looks Wrong

**Symptom:** Elements are too close together or too far apart

**Solutions:**

1. **Understand padding and margin:**
   - **Padding**: Space inside an element (between border and content)
   - **Margin**: Space outside an element (between elements)

2. **Common spacing classes:**
   ```
   p-4 = padding all sides (small)
   p-8 = padding all sides (medium)
   p-12 = padding all sides (large)
   
   m-4 = margin all sides (small)
   m-8 = margin all sides (medium)
   
   gap-4 = space between items (small)
   gap-8 = space between items (medium)
   ```

3. **Example - Adding more space:**
   ```html
   <!-- BEFORE - Less space -->
   <div class="p-4 gap-4">Content</div>
   
   <!-- AFTER - More space -->
   <div class="p-8 gap-8">Content</div>
   ```

---

## Best Practices

### 1. Always Backup Before Making Changes

**Why:** If something breaks, you can revert to the working version

**How:**
1. Before editing, save a copy of your HTML file
2. Name it `index-backup.html` or `index-old.html`
3. Keep this backup safe
4. Only edit the main `index.html`

### 2. Make One Change at a Time

**Why:** If something breaks, you'll know exactly what caused it

**Bad Approach:**
- Change 5 things at once
- Something breaks
- Can't figure out which change caused the problem

**Good Approach:**
- Change one thing
- Test it (refresh browser, check if it works)
- Save
- Move to next change

### 3. Use Meaningful File Names

**Why:** It's easy to find and organize your files

```
❌ Bad names:
- file.html
- index2.html
- new.html

✅ Good names:
- index.html
- privacy.html
- terms.html
- blog.html
- contact.html
```

### 4. Keep All Files in One Folder

**Why:** Simpler to manage and easier to move your website

**Folder Structure:**
```
my-website/
├── index.html
├── privacy.html
├── terms.html
├── blog.html
└── contact.html
```

### 5. Test All Links After Changes

**Checklist:**
- [ ] Navigation menu links work
- [ ] Mobile menu links work
- [ ] All buttons link to correct pages
- [ ] Footer links work
- [ ] Email and phone links work
- [ ] Social media links work (if applicable)

### 6. Use Descriptive Anchor Links

**Why:** Easy to remember and update

```html
❌ Not descriptive:
<section id="s1">Features</section>
<a href="#s1">Click here</a>

✅ Descriptive:
<section id="features">Features</section>
<a href="#features">Our Features</a>
```

### 7. Keep Contact Information Updated

**Why:** Visitors need current ways to reach you

**Update in these locations:**
1. Header (Get Started button)
2. Hero section (buttons)
3. Contact form
4. Footer
5. Privacy and Terms pages

### 8. Test on Mobile Devices

**Why:** Your page should look good on phones and tablets

**How to test:**
1. Open your page on a phone or tablet
2. Check text is readable
3. Check buttons are clickable
4. Check mobile menu works
5. Check images display properly

**If you don't have a device:**
- Use browser developer tools (F12)
- Click the phone icon in top-left
- Select different device sizes

### 9. Validate Your HTML

**Why:** Catches errors that might break your page

**How:**
1. Go to [validator.w3.org](https://validator.w3.org)
2. Upload your HTML file
3. Fix any errors shown

### 10. Keep Backups of Important Content

**Why:** If you accidentally delete something, you can recover it

**What to backup:**
- All HTML files
- Updated text and images
- Contact information
- Testimonials and case information

**How:**
- Use cloud storage (Google Drive, Dropbox, OneDrive)
- Keep local copies on your computer
- Update backups regularly

---

## Common Tasks Quick Reference

### Change Main Headline
**Location:** Line 73
```html
<h1 class="...">We Are Family Advocates for <span class="text-primary">Change</span></h1>
```

### Change Tagline
**Location:** Line 96
```html
<p class="...">Voice for the Voiceless — We Fight GBV & Family Conflict</p>
```

### Update Feature Card Titles
**Location:** Lines 173, 186, 199
```html
<h3 class="text-2xl font-bold text-gray-900 mb-3">TITLE HERE</h3>
```

### Update Testimonials
**Location:** Lines 475-545
Replace client names, titles, and quotes

### Update FAQ
**Location:** Lines 595-700
Replace questions and answers

### Update Footer Email
**Location:** Line 775
```html
<a href="mailto:info@somda.co.za">info@somda.co.za</a>
```

### Update Footer Phone
**Location:** Line 775
```html
<a href="tel:+27123456789">+27 (12) 345-6789</a>
```

### Change Brand Colors
**Location:** Lines 22-28
Update hex codes in `.gradient-primary`, `.text-primary`, `.text-accent`, `.bg-secondary`

---

## Conclusion

You now have all the knowledge needed to maintain and customize your SOMDA landing page. Remember:

1. **Start small** - Make one change at a time
2. **Test often** - Refresh your browser after each change
3. **Keep backups** - Always have a working copy
4. **Ask for help** - If you get stuck, don't hesitate to reach out

For additional resources:
- **HTML Learning:** [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)
- **Tailwind CSS:** [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- **Color Picker:** [colorpicker.com](https://www.colorpicker.com)
- **HTML Validator:** [validator.w3.org](https://validator.w3.org)

Good luck with your website! Your SOMDA landing page is now ready for customization and maintenance.