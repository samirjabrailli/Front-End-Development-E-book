# Comprehensive Front-End Development Guide: A-Z




## Table of Contents

1. [HTML - The Foundation of Web Pages](#html)
2. [CSS - Styling and Layout](#css)
3. [Bootstrap - Rapid UI Development](#bootstrap)
4. [JavaScript - Adding Interactivity](#javascript)
5. [React.js - Building User Interfaces](#react)
6. [Tailwind CSS - Utility-First Styling](#tailwind)
7. [Next.js - Full-Stack React Framework](#nextjs)
8. [References](#references)

---

## HTML - The Foundation of Web Pages {#html}

### What is HTML?

HTML (HyperText Markup Language) is the standard markup language for creating web pages and web applications. It provides the structure and semantic meaning to web content, defining elements such as headings, paragraphs, links, images, forms, and more. HTML works in conjunction with CSS for styling and JavaScript for interactivity to create complete web experiences.

### HTML Document Structure

Every HTML document follows a specific structure that browsers expect. The basic structure includes a DOCTYPE declaration, html element, head section, and body section:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Page description for SEO">
    <meta name="keywords" content="relevant, keywords">
    <title>Page Title</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <h1>Main Heading</h1>
        <nav>
            <ul>
                <li><a href="/">Home</a></li>
                <li><a href="/about">About</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <article>
            <h2>Article Title</h2>
            <p>Article content goes here.</p>
        </article>
    </main>
    
    <footer>
        <p>&copy; 2025 Your Company</p>
    </footer>
    
    <script src="script.js"></script>
</body>
</html>
```

### Semantic HTML Elements

Semantic HTML elements provide meaning to the content they contain, improving accessibility and SEO. Instead of using generic `<div>` elements for everything, semantic elements clearly describe their purpose:

| Element | Purpose |
|---------|---------|
| `<header>` | Introductory content or navigation |
| `<nav>` | Navigation links |
| `<main>` | Main content of the page |
| `<article>` | Self-contained content |
| `<section>` | Thematic grouping of content |
| `<aside>` | Sidebar or supplementary content |
| `<footer>` | Footer information |
| `<figure>` | Self-contained illustration or diagram |
| `<figcaption>` | Caption for a figure |
| `<time>` | Date or time |

### Common HTML Elements

**Text Elements:**
```html
<h1>Heading 1 (Most Important)</h1>
<h2>Heading 2</h2>
<p>Paragraph text</p>
<strong>Bold text (strong importance)</strong>
<em>Italic text (emphasis)</em>
<small>Small text</small>
<mark>Highlighted text</mark>
<code>Inline code</code>
<pre><code>Preformatted code block</code></pre>
```

**Links and Images:**
```html
<a href="https://example.com">Link text</a>
<a href="https://example.com" target="_blank" rel="noopener noreferrer">Open in new tab</a>
<img src="image.jpg" alt="Descriptive alt text" width="300" height="200">
<picture>
    <source media="(min-width: 768px)" srcset="large.jpg">
    <source media="(min-width: 480px)" srcset="medium.jpg">
    <img src="small.jpg" alt="Responsive image">
</picture>
```

**Lists:**
```html
<!-- Unordered list -->
<ul>
    <li>Item 1</li>
    <li>Item 2</li>
    <li>Item 3</li>
</ul>

<!-- Ordered list -->
<ol>
    <li>First step</li>
    <li>Second step</li>
    <li>Third step</li>
</ol>

<!-- Description list -->
<dl>
    <dt>Term</dt>
    <dd>Definition of the term</dd>
</dl>
```

### HTML Forms

Forms are essential for collecting user input. They include various input types and validation attributes:

```html
<form action="/submit" method="POST">
    <!-- Text input -->
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
    
    <!-- Email input with validation -->
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
    
    <!-- Password input -->
    <label for="password">Password:</label>
    <input type="password" id="password" name="password" minlength="8" required>
    
    <!-- Number input -->
    <label for="age">Age:</label>
    <input type="number" id="age" name="age" min="18" max="120">
    
    <!-- Date input -->
    <label for="birthdate">Birth Date:</label>
    <input type="date" id="birthdate" name="birthdate">
    
    <!-- Textarea -->
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="5" cols="40"></textarea>
    
    <!-- Select dropdown -->
    <label for="country">Country:</label>
    <select id="country" name="country">
        <option value="">Select a country</option>
        <option value="us">United States</option>
        <option value="uk">United Kingdom</option>
        <option value="ca">Canada</option>
    </select>
    
    <!-- Radio buttons -->
    <fieldset>
        <legend>Gender:</legend>
        <input type="radio" id="male" name="gender" value="male">
        <label for="male">Male</label>
        <input type="radio" id="female" name="gender" value="female">
        <label for="female">Female</label>
    </fieldset>
    
    <!-- Checkboxes -->
    <fieldset>
        <legend>Interests:</legend>
        <input type="checkbox" id="sports" name="interests" value="sports">
        <label for="sports">Sports</label>
        <input type="checkbox" id="music" name="interests" value="music">
        <label for="music">Music</label>
    </fieldset>
    
    <!-- Buttons -->
    <button type="submit">Submit</button>
    <button type="reset">Reset</button>
    <button type="button">Click me</button>
</form>
```

### HTML Accessibility

Accessibility ensures that web content is usable by everyone, including people with disabilities. Key accessibility practices include:

**ARIA Attributes:**
```html
<!-- ARIA labels for screen readers -->
<button aria-label="Close menu">×</button>
<div role="navigation" aria-label="Main navigation">
    <ul>
        <li><a href="/">Home</a></li>
    </ul>
</div>

<!-- ARIA live regions for dynamic content -->
<div aria-live="polite" aria-atomic="true">
    Loading content...
</div>
```

**Keyboard Navigation:**
```html
<!-- Tab order -->
<input type="text" tabindex="1">
<button tabindex="2">Submit</button>

<!-- Skip to main content link -->
<a href="#main-content" class="skip-link">Skip to main content</a>
<main id="main-content">
    <!-- Main content here -->
</main>
```

### Meta Tags and SEO

Meta tags provide metadata about the HTML document, crucial for SEO and user experience:

```html
<head>
    <!-- Character encoding -->
    <meta charset="UTF-8">
    
    <!-- Viewport for responsive design -->
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Page description (appears in search results) -->
    <meta name="description" content="Brief description of the page content">
    
    <!-- Keywords -->
    <meta name="keywords" content="keyword1, keyword2, keyword3">
    
    <!-- Author -->
    <meta name="author" content="Your Name">
    
    <!-- Open Graph for social media sharing -->
    <meta property="og:title" content="Page Title">
    <meta property="og:description" content="Page description">
    <meta property="og:image" content="image.jpg">
    <meta property="og:url" content="https://example.com">
    
    <!-- Twitter Card -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="Page Title">
    <meta name="twitter:description" content="Page description">
    <meta name="twitter:image" content="image.jpg">
    
    <!-- Favicon -->
    <link rel="icon" type="image/x-icon" href="favicon.ico">
    
    <!-- Canonical URL (prevents duplicate content issues) -->
    <link rel="canonical" href="https://example.com/page">
</head>
```

### HTML Best Practices

1. **Use semantic HTML**: Choose appropriate semantic elements over generic divs
2. **Validate your HTML**: Use the W3C Markup Validator to ensure valid code
3. **Keep it simple**: Avoid unnecessary nesting and complexity
4. **Use meaningful IDs and classes**: Make selectors descriptive and reusable
5. **Optimize images**: Use appropriate formats and sizes
6. **Implement accessibility**: Include alt text, ARIA labels, and keyboard navigation
7. **Mobile-first approach**: Design for mobile first, then enhance for larger screens
8. **Minimize HTTP requests**: Combine files where appropriate

---

## CSS - Styling and Layout {#css}

### CSS Fundamentals

CSS (Cascading Style Sheets) controls the visual presentation of HTML elements. CSS uses selectors to target elements and properties to define their appearance.

### CSS Selectors

CSS selectors determine which HTML elements to style:

```css
/* Element selector */
p { color: blue; }

/* Class selector */
.highlight { background-color: yellow; }

/* ID selector */
#header { background-color: navy; }

/* Attribute selector */
input[type="text"] { border: 1px solid gray; }

/* Pseudo-class selector */
a:hover { color: red; }
button:active { transform: scale(0.95); }
li:first-child { font-weight: bold; }
li:last-child { margin-bottom: 0; }
li:nth-child(2n) { background-color: #f0f0f0; }

/* Pseudo-element selector */
p::first-line { font-weight: bold; }
p::first-letter { font-size: 2em; }
::before { content: "→ "; }
::after { content: " ←"; }

/* Descendant selector */
div p { color: green; }

/* Child selector */
div > p { color: green; }

/* Adjacent sibling selector */
h2 + p { margin-top: 0; }

/* General sibling selector */
h2 ~ p { color: gray; }

/* Multiple selectors */
h1, h2, h3 { font-family: Arial; }

/* Attribute selector variations */
a[href^="https"] { color: green; } /* Starts with */
a[href$=".pdf"] { color: red; } /* Ends with */
a[href*="example"] { color: blue; } /* Contains */
```

### CSS Properties and Values

**Text and Font Properties:**
```css
.text-styling {
    /* Font family */
    font-family: 'Arial', 'Helvetica', sans-serif;
    
    /* Font size */
    font-size: 16px;
    
    /* Font weight */
    font-weight: bold; /* or 400, 700, etc. */
    
    /* Font style */
    font-style: italic;
    
    /* Line height */
    line-height: 1.6;
    
    /* Letter spacing */
    letter-spacing: 2px;
    
    /* Text alignment */
    text-align: center; /* left, right, justify, center */
    
    /* Text decoration */
    text-decoration: underline;
    
    /* Text transform */
    text-transform: uppercase; /* lowercase, capitalize */
    
    /* Color */
    color: #333333;
}
```

**Box Model Properties:**
```css
.box-model {
    /* Margin (outside spacing) */
    margin: 20px;
    margin-top: 10px;
    margin-right: 15px;
    margin-bottom: 10px;
    margin-left: 15px;
    
    /* Padding (inside spacing) */
    padding: 20px;
    padding-top: 10px;
    
    /* Border */
    border: 1px solid #333;
    border-width: 2px;
    border-style: solid;
    border-color: #333;
    border-radius: 8px;
    
    /* Width and height */
    width: 300px;
    height: 200px;
    max-width: 100%;
    min-height: 50px;
    
    /* Box sizing */
    box-sizing: border-box; /* includes padding and border in width/height */
}
```

**Background Properties:**
```css
.background {
    /* Background color */
    background-color: #f0f0f0;
    
    /* Background image */
    background-image: url('image.jpg');
    background-size: cover; /* contain, 100px 200px */
    background-position: center; /* top, bottom, left, right */
    background-repeat: no-repeat; /* repeat, repeat-x, repeat-y */
    background-attachment: fixed; /* scroll, fixed */
    
    /* Shorthand */
    background: #f0f0f0 url('image.jpg') no-repeat center/cover;
}
```

**Display and Positioning:**
```css
.display-positioning {
    /* Display */
    display: block; /* inline, inline-block, flex, grid, none */
    
    /* Position */
    position: static; /* relative, absolute, fixed, sticky */
    top: 10px;
    right: 20px;
    bottom: 10px;
    left: 20px;
    
    /* Z-index (stacking order) */
    z-index: 100;
    
    /* Overflow */
    overflow: auto; /* visible, hidden, scroll, auto */
    overflow-x: hidden;
    overflow-y: auto;
}
```

### Flexbox Layout

Flexbox is a one-dimensional layout method for distributing space and aligning items:

```css
.flex-container {
    display: flex;
    
    /* Main axis direction */
    flex-direction: row; /* column, row-reverse, column-reverse */
    
    /* Wrapping */
    flex-wrap: wrap; /* nowrap, wrap, wrap-reverse */
    
    /* Main axis alignment */
    justify-content: center; /* flex-start, flex-end, center, space-between, space-around, space-evenly */
    
    /* Cross axis alignment */
    align-items: center; /* flex-start, flex-end, center, stretch, baseline */
    
    /* Multiple lines alignment */
    align-content: center; /* flex-start, flex-end, center, space-between, space-around, stretch */
    
    /* Gap between items */
    gap: 20px;
    row-gap: 10px;
    column-gap: 15px;
}

.flex-item {
    /* Growth factor */
    flex-grow: 1;
    
    /* Shrink factor */
    flex-shrink: 1;
    
    /* Base size */
    flex-basis: 200px;
    
    /* Shorthand */
    flex: 1 1 200px;
    
    /* Individual alignment */
    align-self: flex-end;
}
```

**Flexbox Example:**
```html
<style>
    .flex-container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        gap: 20px;
        padding: 20px;
    }
    
    .flex-item {
        flex: 1;
        background-color: #3498db;
        padding: 20px;
        color: white;
        text-align: center;
    }
</style>

<div class="flex-container">
    <div class="flex-item">Item 1</div>
    <div class="flex-item">Item 2</div>
    <div class="flex-item">Item 3</div>
</div>
```

### CSS Grid Layout

CSS Grid is a two-dimensional layout method for creating complex layouts:

```css
.grid-container {
    display: grid;
    
    /* Define columns */
    grid-template-columns: 200px 1fr 200px;
    /* or: repeat(3, 1fr); */
    /* or: repeat(auto-fit, minmax(250px, 1fr)); */
    
    /* Define rows */
    grid-template-rows: auto 1fr auto;
    
    /* Gap between items */
    gap: 20px;
    row-gap: 10px;
    column-gap: 15px;
    
    /* Alignment */
    justify-items: center; /* Horizontal alignment of items */
    align-items: center; /* Vertical alignment of items */
    justify-content: center; /* Horizontal alignment of grid */
    align-content: center; /* Vertical alignment of grid */
}

.grid-item {
    /* Span columns */
    grid-column: 1 / 3; /* or: span 2; */
    
    /* Span rows */
    grid-row: 1 / 3;
    
    /* Individual alignment */
    justify-self: end;
    align-self: start;
}
```

**Grid Example:**
```html
<style>
    .grid-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 20px;
        padding: 20px;
    }
    
    .grid-item {
        background-color: #2ecc71;
        padding: 20px;
        color: white;
        text-align: center;
    }
    
    .grid-item:first-child {
        grid-column: 1 / 3;
    }
</style>

<div class="grid-container">
    <div class="grid-item">Item 1 (spans 2 columns)</div>
    <div class="grid-item">Item 2</div>
    <div class="grid-item">Item 3</div>
    <div class="grid-item">Item 4</div>
</div>
```

### Responsive Design with Media Queries

Media queries allow you to apply different styles based on device characteristics:

```css
/* Mobile-first approach */
.container {
    width: 100%;
    padding: 10px;
}

/* Tablet devices (768px and up) */
@media (min-width: 768px) {
    .container {
        width: 750px;
        padding: 20px;
    }
}

/* Desktop devices (1024px and up) */
@media (min-width: 1024px) {
    .container {
        width: 960px;
        padding: 30px;
    }
}

/* Large desktop (1200px and up) */
@media (min-width: 1200px) {
    .container {
        width: 1140px;
    }
}

/* Print media */
@media print {
    body {
        background-color: white;
        color: black;
    }
    .no-print {
        display: none;
    }
}

/* Orientation */
@media (orientation: landscape) {
    .container {
        height: 100vh;
    }
}

/* Dark mode preference */
@media (prefers-color-scheme: dark) {
    body {
        background-color: #1a1a1a;
        color: #ffffff;
    }
}

/* Reduced motion preference */
@media (prefers-reduced-motion: reduce) {
    * {
        animation-duration: 0.01ms !important;
        animation-iteration-count: 1 !important;
        transition-duration: 0.01ms !important;
    }
}
```

### CSS Transforms and Transitions

**Transforms** modify the appearance and position of elements:

```css
.transform-example {
    /* Translate (move) */
    transform: translate(50px, 100px);
    transform: translateX(50px);
    transform: translateY(100px);
    
    /* Scale (resize) */
    transform: scale(1.5);
    transform: scaleX(2);
    transform: scaleY(0.5);
    
    /* Rotate */
    transform: rotate(45deg);
    
    /* Skew */
    transform: skew(10deg, 20deg);
    transform: skewX(10deg);
    
    /* Multiple transforms */
    transform: translate(50px, 100px) rotate(45deg) scale(1.2);
    
    /* 3D transforms */
    transform: rotateX(45deg);
    transform: rotateY(45deg);
    transform: rotateZ(45deg);
    transform: perspective(1000px) rotateY(45deg);
}
```

**Transitions** create smooth animations between states:

```css
.transition-example {
    background-color: blue;
    color: white;
    padding: 10px 20px;
    
    /* Transition properties */
    transition-property: background-color, color;
    transition-duration: 0.3s;
    transition-timing-function: ease-in-out;
    transition-delay: 0.1s;
    
    /* Shorthand */
    transition: background-color 0.3s ease-in-out 0.1s;
    
    /* Transition all properties */
    transition: all 0.3s ease;
}

.transition-example:hover {
    background-color: red;
    color: yellow;
}
```

**Animations** create keyframe-based animations:

```css
@keyframes slideIn {
    from {
        transform: translateX(-100%);
        opacity: 0;
    }
    to {
        transform: translateX(0);
        opacity: 1;
    }
}

.animated-element {
    animation-name: slideIn;
    animation-duration: 1s;
    animation-timing-function: ease-out;
    animation-delay: 0.2s;
    animation-iteration-count: 1; /* or infinite */
    animation-direction: normal; /* reverse, alternate, alternate-reverse */
    animation-fill-mode: forwards; /* backwards, both */
    
    /* Shorthand */
    animation: slideIn 1s ease-out 0.2s 1 normal forwards;
}
```

### CSS Best Practices

1. **Use external stylesheets**: Keep CSS separate from HTML
2. **Organize with comments**: Group related styles and add clear comments
3. **Use meaningful class names**: Follow BEM or similar naming conventions
4. **Avoid inline styles**: Use classes instead
5. **Minimize specificity**: Use simple, specific selectors
6. **Mobile-first approach**: Start with mobile styles, then enhance
7. **Use CSS variables**: Define reusable values for colors, fonts, etc.
8. **Optimize for performance**: Minimize CSS file size and avoid unnecessary selectors

```css
/* CSS Variables Example */
:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --font-size-base: 16px;
    --spacing-unit: 8px;
}

body {
    font-size: var(--font-size-base);
}

.button {
    background-color: var(--primary-color);
    padding: calc(var(--spacing-unit) * 2);
}

.button.secondary {
    background-color: var(--secondary-color);
}
```

---

## Bootstrap - Rapid UI Development {#bootstrap}

### Introduction to Bootstrap

Bootstrap is a popular open-source CSS framework that provides pre-built components, a responsive grid system, and utility classes for rapidly developing responsive web applications. It uses Flexbox for layouts and includes extensive JavaScript components.

### Bootstrap Installation

**Via CDN (Content Delivery Network):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bootstrap Example</title>
    <!-- Bootstrap CSS -->
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>
    <!-- Content here -->
    
    <!-- Bootstrap JS Bundle (includes Popper) -->
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

**Via npm:**
```bash
npm install bootstrap
```

Then import in your JavaScript:
```javascript
import 'bootstrap/dist/css/bootstrap.css';
import 'bootstrap/dist/js/bootstrap.bundle.js';
```

### Bootstrap Grid System

The Bootstrap grid system is built with Flexbox and uses a 12-column layout:

```html
<div class="container">
    <div class="row">
        <!-- Full width column -->
        <div class="col-12">
            Full width
        </div>
    </div>
    
    <div class="row">
        <!-- Two equal columns -->
        <div class="col-6">
            Half width
        </div>
        <div class="col-6">
            Half width
        </div>
    </div>
    
    <div class="row">
        <!-- Three equal columns -->
        <div class="col-4">
            One third
        </div>
        <div class="col-4">
            One third
        </div>
        <div class="col-4">
            One third
        </div>
    </div>
</div>
```

**Responsive Grid:**
```html
<div class="container">
    <div class="row">
        <!-- Mobile: full width, Tablet (768px+): half width, Desktop (992px+): one third -->
        <div class="col-12 col-md-6 col-lg-4">
            Responsive column
        </div>
        <div class="col-12 col-md-6 col-lg-4">
            Responsive column
        </div>
        <div class="col-12 col-md-6 col-lg-4">
            Responsive column
        </div>
    </div>
</div>
```

**Bootstrap Breakpoints:**

| Breakpoint | Class Infix | Dimensions |
|-----------|-----------|-----------|
| Extra small | None | < 576px |
| Small | `sm` | ≥ 576px |
| Medium | `md` | ≥ 768px |
| Large | `lg` | ≥ 992px |
| Extra large | `xl` | ≥ 1200px |
| XXL | `xxl` | ≥ 1400px |

### Bootstrap Components

**Buttons:**
```html
<!-- Button styles -->
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-success">Success</button>
<button class="btn btn-danger">Danger</button>
<button class="btn btn-warning">Warning</button>
<button class="btn btn-info">Info</button>

<!-- Button sizes -->
<button class="btn btn-primary btn-lg">Large</button>
<button class="btn btn-primary">Normal</button>
<button class="btn btn-primary btn-sm">Small</button>

<!-- Button states -->
<button class="btn btn-primary" disabled>Disabled</button>
<button class="btn btn-primary active">Active</button>

<!-- Button groups -->
<div class="btn-group" role="group">
    <button type="button" class="btn btn-outline-primary">Left</button>
    <button type="button" class="btn btn-outline-primary">Middle</button>
    <button type="button" class="btn btn-outline-primary">Right</button>
</div>
```

**Cards:**
```html
<div class="card" style="width: 18rem;">
    <img src="image.jpg" class="card-img-top" alt="...">
    <div class="card-body">
        <h5 class="card-title">Card Title</h5>
        <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
        <a href="#" class="btn btn-primary">Go somewhere</a>
    </div>
    <div class="card-footer text-muted">
        Last updated 3 mins ago
    </div>
</div>

<!-- Card with list -->
<div class="card">
    <div class="card-header">
        Featured
    </div>
    <ul class="list-group list-group-flush">
        <li class="list-group-item">An item</li>
        <li class="list-group-item">A second item</li>
        <li class="list-group-item">A third item</li>
    </ul>
</div>
```

**Navigation Bar:**
```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
    <div class="container-fluid">
        <a class="navbar-brand" href="#">Navbar</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
            <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
            <ul class="navbar-nav ms-auto">
                <li class="nav-item">
                    <a class="nav-link active" href="#">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Features</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown">
                        Dropdown
                    </a>
                    <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <li><a class="dropdown-item" href="#">Action</a></li>
                        <li><a class="dropdown-item" href="#">Another action</a></li>
                        <li><hr class="dropdown-divider"></li>
                        <li><a class="dropdown-item" href="#">Something else here</a></li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</nav>
```

**Forms:**
```html
<form>
    <div class="mb-3">
        <label for="exampleInputEmail1" class="form-label">Email address</label>
        <input type="email" class="form-control" id="exampleInputEmail1" aria-describedby="emailHelp">
        <div id="emailHelp" class="form-text">We'll never share your email with anyone else.</div>
    </div>
    
    <div class="mb-3">
        <label for="exampleInputPassword1" class="form-label">Password</label>
        <input type="password" class="form-control" id="exampleInputPassword1">
    </div>
    
    <div class="mb-3 form-check">
        <input type="checkbox" class="form-check-input" id="exampleCheck1">
        <label class="form-check-label" for="exampleCheck1">
            Check me out
        </label>
    </div>
    
    <button type="submit" class="btn btn-primary">Submit</button>
</form>
```

**Alerts:**
```html
<div class="alert alert-primary" role="alert">
    A simple primary alert—check it out!
</div>
<div class="alert alert-success" role="alert">
    A simple success alert—check it out!
</div>
<div class="alert alert-danger alert-dismissible fade show" role="alert">
    <strong>Holy guacamole!</strong> You should check in on some of those fields below.
    <button type="button" class="btn-close" data-bs-dismiss="alert" aria-label="Close"></button>
</div>
```

**Modal:**
```html
<!-- Button trigger modal -->
<button type="button" class="btn btn-primary" data-bs-toggle="modal" data-bs-target="#exampleModal">
    Launch demo modal
</button>

<!-- Modal -->
<div class="modal fade" id="exampleModal" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog">
        <div class="modal-content">
            <div class="modal-header">
                <h1 class="modal-title fs-5" id="exampleModalLabel">Modal title</h1>
                <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
            </div>
            <div class="modal-body">
                ...
            </div>
            <div class="modal-footer">
                <button type="button" class="btn btn-secondary" data-bs-dismiss="modal">Close</button>
                <button type="button" class="btn btn-primary">Save changes</button>
            </div>
        </div>
    </div>
</div>
```

### Bootstrap Utilities

Bootstrap provides utility classes for common styling tasks:

```html
<!-- Spacing utilities -->
<div class="m-5">Margin 5</div> <!-- All sides -->
<div class="mt-3">Margin top 3</div>
<div class="p-4">Padding 4</div>

<!-- Display utilities -->
<div class="d-none d-md-block">Hidden on mobile, visible on tablet+</div>
<div class="d-flex justify-content-center">Flexbox centered</div>

<!-- Text utilities -->
<p class="text-center">Centered text</p>
<p class="text-primary">Primary color text</p>
<p class="text-muted">Muted text</p>
<p class="fw-bold">Bold text</p>
<p class="fs-5">Font size 5</p>

<!-- Color utilities -->
<div class="bg-primary text-white">Primary background</div>
<div class="bg-light text-dark">Light background</div>

<!-- Border utilities -->
<div class="border">Border on all sides</div>
<div class="border-top border-danger">Top border in danger color</div>
<div class="rounded">Rounded corners</div>
<div class="rounded-circle">Circle</div>
```

### Bootstrap Best Practices

1. **Use the grid system**: Build responsive layouts with the 12-column grid
2. **Leverage components**: Use pre-built components instead of creating from scratch
3. **Customize Bootstrap**: Override default variables for your brand colors
4. **Minimize custom CSS**: Use utilities first before writing custom styles
5. **Mobile-first**: Design for mobile, then enhance for larger screens
6. **Accessibility**: Use semantic HTML and ARIA attributes
7. **Performance**: Only include the Bootstrap components you need

---

## JavaScript - Adding Interactivity {#javascript}

### JavaScript Fundamentals

JavaScript is a versatile programming language that runs in browsers and on servers (Node.js). It enables interactive web pages and complex web applications.

### Variables and Data Types

```javascript
// Variable declaration
var oldWay = 'avoid using var';
let variableName = 'can be reassigned';
const constantValue = 'cannot be reassigned';

// Data types
const string = 'Hello, World!';
const number = 42;
const decimal = 3.14;
const boolean = true;
const nullValue = null;
const undefinedValue = undefined;
const symbol = Symbol('unique');
const bigInt = 123456789012345678901234567890n;

// Objects
const person = {
    name: 'John',
    age: 30,
    email: 'john@example.com',
    address: {
        street: '123 Main St',
        city: 'New York'
    }
};

// Arrays
const numbers = [1, 2, 3, 4, 5];
const mixed = [1, 'two', true, { key: 'value' }];

// Template literals
const name = 'Alice';
const greeting = `Hello, ${name}! You are ${30 + 5} years old.`;
```

### Functions

```javascript
// Function declaration
function add(a, b) {
    return a + b;
}

// Function expression
const multiply = function(a, b) {
    return a * b;
};

// Arrow function (ES6)
const subtract = (a, b) => a - b;
const divide = (a, b) => {
    if (b === 0) {
        return 'Cannot divide by zero';
    }
    return a / b;
};

// Function with default parameters
const greet = (name = 'Guest') => {
    return `Hello, ${name}!`;
};

// Function with rest parameters
const sum = (...numbers) => {
    return numbers.reduce((total, num) => total + num, 0);
};

// Function with destructuring
const displayPerson = ({ name, age, email }) => {
    console.log(`${name} is ${age} years old and can be reached at ${email}`);
};

// Immediately Invoked Function Expression (IIFE)
(function() {
    console.log('This runs immediately');
})();

// Higher-order function
const createMultiplier = (multiplier) => {
    return (number) => number * multiplier;
};

const double = createMultiplier(2);
console.log(double(5)); // 10
```

### DOM Manipulation

The Document Object Model (DOM) represents the HTML structure as a tree of objects that JavaScript can manipulate:

```javascript
// Selecting elements
const element = document.getElementById('myId');
const elements = document.getElementsByClassName('myClass');
const element2 = document.querySelector('.myClass');
const elements2 = document.querySelectorAll('p.myClass');

// Creating elements
const newDiv = document.createElement('div');
newDiv.textContent = 'Hello, World!';
newDiv.className = 'my-class';
newDiv.id = 'my-id';
newDiv.setAttribute('data-value', '123');

// Modifying elements
element.textContent = 'New text content';
element.innerHTML = '<strong>Bold text</strong>';
element.style.color = 'red';
element.style.backgroundColor = '#f0f0f0';
element.classList.add('active');
element.classList.remove('inactive');
element.classList.toggle('highlighted');

// Appending elements
document.body.appendChild(newDiv);
parentElement.insertBefore(newDiv, referenceElement);
element.insertAdjacentHTML('beforeend', '<p>New paragraph</p>');

// Removing elements
element.remove();
parentElement.removeChild(element);

// Getting element properties
const value = element.value; // For input elements
const text = element.textContent;
const html = element.innerHTML;
const classes = element.classList;
const attributes = element.attributes;
```

### Event Handling

```javascript
// Adding event listeners
const button = document.getElementById('myButton');

button.addEventListener('click', function(event) {
    console.log('Button clicked!');
    console.log(event.target);
    console.log(event.type);
});

// Arrow function in event listener
button.addEventListener('click', (event) => {
    console.log('Button clicked with arrow function');
});

// Common events
document.addEventListener('DOMContentLoaded', () => {
    console.log('DOM is fully loaded');
});

window.addEventListener('load', () => {
    console.log('All resources loaded');
});

window.addEventListener('resize', () => {
    console.log('Window resized');
});

document.addEventListener('scroll', () => {
    console.log('Page scrolled');
});

const input = document.getElementById('myInput');
input.addEventListener('input', (event) => {
    console.log('Input value:', event.target.value);
});

input.addEventListener('change', (event) => {
    console.log('Input changed:', event.target.value);
});

input.addEventListener('focus', () => {
    console.log('Input focused');
});

input.addEventListener('blur', () => {
    console.log('Input lost focus');
});

// Event delegation
const list = document.getElementById('myList');
list.addEventListener('click', (event) => {
    if (event.target.tagName === 'LI') {
        console.log('List item clicked:', event.target.textContent);
    }
});

// Removing event listeners
const handler = () => console.log('Clicked');
button.addEventListener('click', handler);
button.removeEventListener('click', handler);

// Preventing default behavior
const link = document.getElementById('myLink');
link.addEventListener('click', (event) => {
    event.preventDefault();
    console.log('Link click prevented');
});

// Stopping event propagation
button.addEventListener('click', (event) => {
    event.stopPropagation();
    console.log('Event propagation stopped');
});
```

### ES6+ Features

**Destructuring:**
```javascript
// Array destructuring
const [first, second, third] = [1, 2, 3];
const [a, , c] = [1, 2, 3]; // Skip middle element

// Object destructuring
const { name, age, email } = { name: 'John', age: 30, email: 'john@example.com' };
const { name: fullName, age: years } = person; // Rename properties

// Nested destructuring
const { address: { city } } = person;

// Default values
const { role = 'user' } = {}; // role will be 'user'
```

**Spread Operator:**
```javascript
// Array spreading
const arr1 = [1, 2, 3];
const arr2 = [4, 5, 6];
const combined = [...arr1, ...arr2]; // [1, 2, 3, 4, 5, 6]

// Object spreading
const obj1 = { a: 1, b: 2 };
const obj2 = { c: 3, d: 4 };
const merged = { ...obj1, ...obj2 }; // { a: 1, b: 2, c: 3, d: 4 }

// Function arguments
const numbers = [1, 2, 3];
Math.max(...numbers); // 3
```

**Rest Parameters:**
```javascript
const sum = (...numbers) => {
    return numbers.reduce((total, num) => total + num, 0);
};

sum(1, 2, 3, 4, 5); // 15
```

**Classes:**
```javascript
class Animal {
    constructor(name) {
        this.name = name;
    }
    
    speak() {
        console.log(`${this.name} makes a sound`);
    }
    
    static info() {
        console.log('This is the Animal class');
    }
}

class Dog extends Animal {
    constructor(name, breed) {
        super(name);
        this.breed = breed;
    }
    
    speak() {
        console.log(`${this.name} barks`);
    }
}

const dog = new Dog('Rex', 'Labrador');
dog.speak(); // Rex barks
Dog.info(); // This is the Animal class
```

### Asynchronous JavaScript

**Promises:**
```javascript
// Creating a promise
const myPromise = new Promise((resolve, reject) => {
    setTimeout(() => {
        resolve('Success!');
    }, 1000);
});

// Using a promise
myPromise
    .then(result => console.log(result))
    .catch(error => console.error(error))
    .finally(() => console.log('Done'));

// Promise chaining
fetch('https://api.example.com/data')
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error('Error:', error));
```

**Async/Await:**
```javascript
// Async function
async function fetchData() {
    try {
        const response = await fetch('https://api.example.com/data');
        const data = await response.json();
        console.log(data);
        return data;
    } catch (error) {
        console.error('Error:', error);
    }
}

// Calling async function
fetchData();

// Async function with multiple awaits
async function processData() {
    try {
        const response1 = await fetch('https://api.example.com/data1');
        const data1 = await response1.json();
        
        const response2 = await fetch('https://api.example.com/data2');
        const data2 = await response2.json();
        
        return { data1, data2 };
    } catch (error) {
        console.error('Error:', error);
    }
}

// Parallel requests
async function parallelRequests() {
    try {
        const [response1, response2] = await Promise.all([
            fetch('https://api.example.com/data1'),
            fetch('https://api.example.com/data2')
        ]);
        
        const [data1, data2] = await Promise.all([
            response1.json(),
            response2.json()
        ]);
        
        return { data1, data2 };
    } catch (error) {
        console.error('Error:', error);
    }
}
```

### Array Methods

```javascript
const numbers = [1, 2, 3, 4, 5];

// map - transform each element
const doubled = numbers.map(num => num * 2); // [2, 4, 6, 8, 10]

// filter - keep elements that match condition
const evens = numbers.filter(num => num % 2 === 0); // [2, 4]

// reduce - accumulate values
const sum = numbers.reduce((total, num) => total + num, 0); // 15

// find - get first element matching condition
const firstEven = numbers.find(num => num % 2 === 0); // 2

// findIndex - get index of first element matching condition
const index = numbers.findIndex(num => num > 3); // 3

// some - check if any element matches condition
const hasEven = numbers.some(num => num % 2 === 0); // true

// every - check if all elements match condition
const allPositive = numbers.every(num => num > 0); // true

// includes - check if array contains value
const includes3 = numbers.includes(3); // true

// join - convert array to string
const str = numbers.join(', '); // "1, 2, 3, 4, 5"

// slice - get portion of array
const slice = numbers.slice(1, 4); // [2, 3, 4]

// splice - modify array in place
const removed = numbers.splice(2, 2); // removes 2 elements starting at index 2

// forEach - iterate over elements
numbers.forEach((num, index) => {
    console.log(`Index ${index}: ${num}`);
});

// sort - sort array
const sorted = [3, 1, 4, 1, 5].sort((a, b) => a - b); // [1, 1, 3, 4, 5]

// reverse - reverse array
const reversed = [1, 2, 3].reverse(); // [3, 2, 1]
```

### Object Methods

```javascript
const person = {
    name: 'John',
    age: 30,
    email: 'john@example.com'
};

// Object.keys - get all keys
const keys = Object.keys(person); // ['name', 'age', 'email']

// Object.values - get all values
const values = Object.values(person); // ['John', 30, 'john@example.com']

// Object.entries - get key-value pairs
const entries = Object.entries(person);
// [['name', 'John'], ['age', 30], ['email', 'john@example.com']]

// Object.assign - merge objects
const merged = Object.assign({}, person, { age: 31 });

// Object.freeze - make object immutable
const frozen = Object.freeze(person);
// frozen.age = 31; // This will not work

// Object.seal - prevent adding/removing properties
const sealed = Object.seal(person);
// sealed.phone = '123-456-7890'; // This will not work
// sealed.age = 31; // This will work

// Object.create - create object with specific prototype
const proto = { greet: () => 'Hello' };
const obj = Object.create(proto);

// Object.defineProperty - define property with descriptor
Object.defineProperty(person, 'phone', {
    value: '123-456-7890',
    writable: false,
    enumerable: true,
    configurable: false
});
```

### Error Handling

```javascript
// Try-catch-finally
try {
    const result = riskyFunction();
    console.log(result);
} catch (error) {
    console.error('Error caught:', error.message);
} finally {
    console.log('Cleanup code');
}

// Custom error
class ValidationError extends Error {
    constructor(message) {
        super(message);
        this.name = 'ValidationError';
    }
}

try {
    throw new ValidationError('Invalid input');
} catch (error) {
    if (error instanceof ValidationError) {
        console.error('Validation error:', error.message);
    }
}

// Throwing errors
function validateEmail(email) {
    if (!email.includes('@')) {
        throw new Error('Invalid email address');
    }
    return email;
}

try {
    validateEmail('invalid-email');
} catch (error) {
    console.error(error.message);
}
```

### JavaScript Best Practices

1. **Use const by default**: Only use let when you need to reassign
2. **Avoid global variables**: Use modules and scoping
3. **Use meaningful names**: Make code self-documenting
4. **Keep functions small**: Single responsibility principle
5. **Use async/await**: Cleaner than promise chains
6. **Handle errors**: Always use try-catch for error-prone operations
7. **Optimize performance**: Avoid unnecessary DOM manipulation
8. **Use strict mode**: Add 'use strict' at the top of files

---

## React.js - Building User Interfaces {#react}

### React Fundamentals

React is a JavaScript library for building user interfaces with reusable components. It uses a virtual DOM for efficient updates and follows a declarative programming paradigm.

### JSX - JavaScript XML

JSX is a syntax extension that allows you to write HTML-like code in JavaScript:

```jsx
// JSX element
const element = <h1>Hello, World!</h1>;

// JSX with expressions
const name = 'Alice';
const greeting = <h1>Hello, {name}!</h1>;

// JSX with attributes
const button = <button className="btn" onClick={handleClick}>Click me</button>;

// JSX with children
const card = (
    <div className="card">
        <h2>Card Title</h2>
        <p>Card content</p>
    </div>
);

// JSX with conditional rendering
const user = { name: 'John', isAdmin: true };
const adminPanel = user.isAdmin ? <div>Admin Panel</div> : <div>User Panel</div>;

// JSX with loops
const items = ['Apple', 'Banana', 'Orange'];
const list = (
    <ul>
        {items.map((item, index) => (
            <li key={index}>{item}</li>
        ))}
    </ul>
);

// JSX with fragments
const fragment = (
    <>
        <h1>Title</h1>
        <p>Content</p>
    </>
);
```

### Functional Components

Functional components are JavaScript functions that return JSX:

```jsx
// Simple functional component
function Welcome() {
    return <h1>Welcome to React!</h1>;
}

// Functional component with props
function Greeting({ name, age }) {
    return <h1>Hello, {name}! You are {age} years old.</h1>;
}

// Functional component with default props
function Button({ label = 'Click me', onClick }) {
    return <button onClick={onClick}>{label}</button>;
}

// Using components
export default function App() {
    const handleClick = () => alert('Button clicked!');
    
    return (
        <div>
            <Welcome />
            <Greeting name="Alice" age={30} />
            <Button label="Submit" onClick={handleClick} />
        </div>
    );
}
```

### Hooks - useState

The useState hook allows functional components to have state:

```jsx
import { useState } from 'react';

function Counter() {
    const [count, setCount] = useState(0);
    
    return (
        <div>
            <p>Count: {count}</p>
            <button onClick={() => setCount(count + 1)}>Increment</button>
            <button onClick={() => setCount(count - 1)}>Decrement</button>
        </div>
    );
}

// Multiple state variables
function Form() {
    const [name, setName] = useState('');
    const [email, setEmail] = useState('');
    const [age, setAge] = useState('');
    
    const handleSubmit = (e) => {
        e.preventDefault();
        console.log({ name, email, age });
    };
    
    return (
        <form onSubmit={handleSubmit}>
            <input
                type="text"
                value={name}
                onChange={(e) => setName(e.target.value)}
                placeholder="Name"
            />
            <input
                type="email"
                value={email}
                onChange={(e) => setEmail(e.target.value)}
                placeholder="Email"
            />
            <input
                type="number"
                value={age}
                onChange={(e) => setAge(e.target.value)}
                placeholder="Age"
            />
            <button type="submit">Submit</button>
        </form>
    );
}

// Using object state
function UserProfile() {
    const [user, setUser] = useState({
        name: 'John',
        email: 'john@example.com',
        age: 30
    });
    
    const updateUser = (field, value) => {
        setUser({
            ...user,
            [field]: value
        });
    };
    
    return (
        <div>
            <p>Name: {user.name}</p>
            <button onClick={() => updateUser('name', 'Jane')}>Change Name</button>
        </div>
    );
}
```

### Hooks - useEffect

The useEffect hook handles side effects like data fetching, subscriptions, and DOM updates:

```jsx
import { useState, useEffect } from 'react';

// Run effect after every render
function Example1() {
    useEffect(() => {
        console.log('Component rendered');
    });
    
    return <div>Example 1</div>;
}

// Run effect only once (on mount)
function Example2() {
    useEffect(() => {
        console.log('Component mounted');
        
        return () => {
            console.log('Component unmounted');
        };
    }, []);
    
    return <div>Example 2</div>;
}

// Run effect when dependencies change
function Example3({ userId }) {
    const [user, setUser] = useState(null);
    
    useEffect(() => {
        fetch(`/api/users/${userId}`)
            .then(res => res.json())
            .then(data => setUser(data));
    }, [userId]); // Re-run when userId changes
    
    return <div>{user ? user.name : 'Loading...'}</div>;
}

// Data fetching example
function UserList() {
    const [users, setUsers] = useState([]);
    const [loading, setLoading] = useState(true);
    const [error, setError] = useState(null);
    
    useEffect(() => {
        const fetchUsers = async () => {
            try {
                const response = await fetch('/api/users');
                const data = await response.json();
                setUsers(data);
            } catch (err) {
                setError(err.message);
            } finally {
                setLoading(false);
            }
        };
        
        fetchUsers();
    }, []);
    
    if (loading) return <div>Loading...</div>;
    if (error) return <div>Error: {error}</div>;
    
    return (
        <ul>
            {users.map(user => (
                <li key={user.id}>{user.name}</li>
            ))}
        </ul>
    );
}

// Cleanup example
function Timer() {
    const [seconds, setSeconds] = useState(0);
    
    useEffect(() => {
        const interval = setInterval(() => {
            setSeconds(s => s + 1);
        }, 1000);
        
        return () => clearInterval(interval); // Cleanup
    }, []);
    
    return <div>Seconds: {seconds}</div>;
}
```

### Hooks - useContext

The useContext hook allows you to access context values without prop drilling:

```jsx
import { createContext, useContext, useState } from 'react';

// Create context
const ThemeContext = createContext();

// Provider component
function ThemeProvider({ children }) {
    const [theme, setTheme] = useState('light');
    
    const toggleTheme = () => {
        setTheme(theme === 'light' ? 'dark' : 'light');
    };
    
    return (
        <ThemeContext.Provider value={{ theme, toggleTheme }}>
            {children}
        </ThemeContext.Provider>
    );
}

// Using context
function ThemedButton() {
    const { theme, toggleTheme } = useContext(ThemeContext);
    
    return (
        <button
            onClick={toggleTheme}
            style={{
                backgroundColor: theme === 'light' ? '#fff' : '#333',
                color: theme === 'light' ? '#000' : '#fff'
            }}
        >
            Toggle Theme
        </button>
    );
}

// App with provider
function App() {
    return (
        <ThemeProvider>
            <ThemedButton />
        </ThemeProvider>
    );
}
```

### Hooks - useReducer

The useReducer hook is useful for complex state logic:

```jsx
import { useReducer } from 'react';

const initialState = { count: 0 };

function reducer(state, action) {
    switch (action.type) {
        case 'INCREMENT':
            return { count: state.count + 1 };
        case 'DECREMENT':
            return { count: state.count - 1 };
        case 'RESET':
            return { count: 0 };
        default:
            return state;
    }
}

function Counter() {
    const [state, dispatch] = useReducer(reducer, initialState);
    
    return (
        <div>
            <p>Count: {state.count}</p>
            <button onClick={() => dispatch({ type: 'INCREMENT' })}>+</button>
            <button onClick={() => dispatch({ type: 'DECREMENT' })}>-</button>
            <button onClick={() => dispatch({ type: 'RESET' })}>Reset</button>
        </div>
    );
}
```

### Custom Hooks

You can create custom hooks to reuse stateful logic:

```jsx
import { useState, useEffect } from 'react';

// Custom hook for fetching data
function useFetch(url) {
    const [data, setData] = useState(null);
    const [loading, setLoading] = useState(true);
    const [error, setError] = useState(null);
    
    useEffect(() => {
        const fetchData = async () => {
            try {
                const response = await fetch(url);
                const json = await response.json();
                setData(json);
            } catch (err) {
                setError(err);
            } finally {
                setLoading(false);
            }
        };
        
        fetchData();
    }, [url]);
    
    return { data, loading, error };
}

// Using custom hook
function UserProfile({ userId }) {
    const { data: user, loading, error } = useFetch(`/api/users/${userId}`);
    
    if (loading) return <div>Loading...</div>;
    if (error) return <div>Error: {error.message}</div>;
    
    return <div>{user.name}</div>;
}

// Custom hook for form handling
function useForm(initialValues, onSubmit) {
    const [values, setValues] = useState(initialValues);
    
    const handleChange = (e) => {
        const { name, value } = e.target;
        setValues({
            ...values,
            [name]: value
        });
    };
    
    const handleSubmit = (e) => {
        e.preventDefault();
        onSubmit(values);
    };
    
    return { values, handleChange, handleSubmit };
}

// Using form hook
function LoginForm() {
    const { values, handleChange, handleSubmit } = useForm(
        { email: '', password: '' },
        (values) => console.log('Submitting:', values)
    );
    
    return (
        <form onSubmit={handleSubmit}>
            <input
                type="email"
                name="email"
                value={values.email}
                onChange={handleChange}
            />
            <input
                type="password"
                name="password"
                value={values.password}
                onChange={handleChange}
            />
            <button type="submit">Login</button>
        </form>
    );
}
```

### Component Composition

React encourages building UIs with composable components:

```jsx
// Presentational component
function Button({ label, onClick, variant = 'primary' }) {
    return (
        <button
            onClick={onClick}
            className={`btn btn-${variant}`}
        >
            {label}
        </button>
    );
}

// Container component
function LoginContainer() {
    const [email, setEmail] = useState('');
    const [password, setPassword] = useState('');
    
    const handleLogin = async () => {
        // Login logic
    };
    
    return (
        <LoginForm
            email={email}
            password={password}
            onEmailChange={setEmail}
            onPasswordChange={setPassword}
            onSubmit={handleLogin}
        />
    );
}

// Reusable form component
function LoginForm({
    email,
    password,
    onEmailChange,
    onPasswordChange,
    onSubmit
}) {
    return (
        <form onSubmit={onSubmit}>
            <input
                type="email"
                value={email}
                onChange={(e) => onEmailChange(e.target.value)}
            />
            <input
                type="password"
                value={password}
                onChange={(e) => onPasswordChange(e.target.value)}
            />
            <Button label="Login" onClick={onSubmit} />
        </form>
    );
}

// Render props pattern
function DataFetcher({ url, children }) {
    const { data, loading, error } = useFetch(url);
    return children({ data, loading, error });
}

// Using render props
function App() {
    return (
        <DataFetcher url="/api/users">
            {({ data, loading, error }) => (
                <>
                    {loading && <div>Loading...</div>}
                    {error && <div>Error: {error.message}</div>}
                    {data && <UserList users={data} />}
                </>
            )}
        </DataFetcher>
    );
}
```

### React Best Practices

1. **Use functional components**: Prefer functional components with hooks
2. **Keep components small**: Single responsibility principle
3. **Lift state up**: Share state between components through parent
4. **Use keys in lists**: Always provide unique keys for list items
5. **Memoize expensive computations**: Use useMemo for performance
6. **Avoid inline functions**: Define functions outside JSX
7. **Use PropTypes or TypeScript**: Validate component props
8. **Optimize re-renders**: Use React.memo and useCallback

---

## Tailwind CSS - Utility-First Styling {#tailwind}

### Introduction to Tailwind CSS

Tailwind CSS is a utility-first CSS framework that provides low-level utility classes for building custom designs directly in HTML. Instead of writing CSS classes with semantic names, you compose utilities to build components.

### Installation

**Via npm:**
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

**Configure tailwind.config.js:**
```javascript
module.exports = {
    content: [
        "./index.html",
        "./src/**/*.{js,ts,jsx,tsx}",
    ],
    theme: {
        extend: {
            colors: {
                primary: '#3b82f6',
                secondary: '#10b981',
            },
            spacing: {
                '128': '32rem',
            },
        },
    },
    plugins: [],
}
```

**Add to CSS file:**
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

### Tailwind Utility Classes

**Spacing (Margin and Padding):**
```html
<!-- Margin -->
<div class="m-4">Margin on all sides</div>
<div class="mt-4">Margin top</div>
<div class="mx-auto">Horizontal centering</div>

<!-- Padding -->
<div class="p-6">Padding on all sides</div>
<div class="px-4 py-2">Horizontal and vertical padding</div>

<!-- Negative margin -->
<div class="-m-2">Negative margin</div>
```

**Display and Layout:**
```html
<!-- Display -->
<div class="block">Block element</div>
<div class="inline">Inline element</div>
<div class="inline-block">Inline block element</div>
<div class="flex">Flexbox container</div>
<div class="grid">Grid container</div>
<div class="hidden">Hidden element</div>

<!-- Flexbox -->
<div class="flex justify-center items-center">
    Centered content
</div>
<div class="flex gap-4">
    <div>Item 1</div>
    <div>Item 2</div>
</div>

<!-- Grid -->
<div class="grid grid-cols-3 gap-4">
    <div>Column 1</div>
    <div>Column 2</div>
    <div>Column 3</div>
</div>
```

**Typography:**
```html
<!-- Font size -->
<p class="text-xs">Extra small</p>
<p class="text-sm">Small</p>
<p class="text-base">Base</p>
<p class="text-lg">Large</p>
<p class="text-xl">Extra large</p>
<p class="text-2xl">2XL</p>

<!-- Font weight -->
<p class="font-light">Light</p>
<p class="font-normal">Normal</p>
<p class="font-semibold">Semibold</p>
<p class="font-bold">Bold</p>

<!-- Text alignment -->
<p class="text-left">Left aligned</p>
<p class="text-center">Center aligned</p>
<p class="text-right">Right aligned</p>

<!-- Text color -->
<p class="text-gray-900">Dark gray text</p>
<p class="text-blue-600">Blue text</p>
<p class="text-red-500">Red text</p>

<!-- Line height -->
<p class="leading-tight">Tight line height</p>
<p class="leading-normal">Normal line height</p>
<p class="leading-relaxed">Relaxed line height</p>
```

**Colors:**
```html
<!-- Background colors -->
<div class="bg-white">White background</div>
<div class="bg-gray-100">Light gray background</div>
<div class="bg-blue-500">Blue background</div>
<div class="bg-red-600">Red background</div>

<!-- Text colors -->
<p class="text-white">White text</p>
<p class="text-gray-700">Gray text</p>
<p class="text-blue-500">Blue text</p>

<!-- Border colors -->
<div class="border-2 border-gray-300">Gray border</div>
<div class="border-2 border-blue-500">Blue border</div>
```

**Borders and Shadows:**
```html
<!-- Borders -->
<div class="border">Border on all sides</div>
<div class="border-t-2">Top border</div>
<div class="border-l-4">Left border</div>
<div class="rounded">Rounded corners</div>
<div class="rounded-lg">Large rounded corners</div>
<div class="rounded-full">Circular</div>

<!-- Shadows -->
<div class="shadow">Small shadow</div>
<div class="shadow-md">Medium shadow</div>
<div class="shadow-lg">Large shadow</div>
<div class="shadow-xl">Extra large shadow</div>
```

**Responsive Design:**
```html
<!-- Mobile-first responsive classes -->
<div class="w-full md:w-1/2 lg:w-1/3">
    Full width on mobile, half on tablet, third on desktop
</div>

<div class="text-sm md:text-base lg:text-lg">
    Small text on mobile, base on tablet, large on desktop
</div>

<div class="flex flex-col md:flex-row gap-4">
    Stacked on mobile, side-by-side on tablet and desktop
</div>

<!-- Hiding elements at different breakpoints -->
<div class="hidden md:block">
    Hidden on mobile, visible on tablet and desktop
</div>

<div class="block md:hidden">
    Visible on mobile, hidden on tablet and desktop
</div>
```

**Hover, Focus, and Active States:**
```html
<!-- Hover -->
<button class="bg-blue-500 hover:bg-blue-700">
    Hover me
</button>

<!-- Focus -->
<input class="border border-gray-300 focus:border-blue-500 focus:outline-none" />

<!-- Active -->
<button class="bg-blue-500 active:bg-blue-900">
    Press me
</button>

<!-- Group hover -->
<div class="group border border-gray-300 hover:bg-blue-500">
    <p class="text-gray-900 group-hover:text-white">
        Text changes on parent hover
    </p>
</div>
```

### Building Components with Tailwind

```html
<!-- Button component -->
<button class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-700 transition">
    Click me
</button>

<!-- Card component -->
<div class="bg-white rounded-lg shadow-md p-6">
    <h2 class="text-xl font-bold mb-2">Card Title</h2>
    <p class="text-gray-600 mb-4">Card description</p>
    <button class="px-4 py-2 bg-blue-500 text-white rounded">
        Action
    </button>
</div>

<!-- Navigation bar -->
<nav class="bg-gray-900 text-white p-4">
    <div class="flex justify-between items-center">
        <h1 class="text-2xl font-bold">Logo</h1>
        <ul class="flex gap-6">
            <li><a href="#" class="hover:text-gray-300">Home</a></li>
            <li><a href="#" class="hover:text-gray-300">About</a></li>
            <li><a href="#" class="hover:text-gray-300">Contact</a></li>
        </ul>
    </div>
</nav>

<!-- Form -->
<form class="max-w-md mx-auto p-6 bg-white rounded-lg shadow">
    <div class="mb-4">
        <label class="block text-gray-700 font-bold mb-2">Name</label>
        <input type="text" class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-blue-500" />
    </div>
    <div class="mb-4">
        <label class="block text-gray-700 font-bold mb-2">Email</label>
        <input type="email" class="w-full px-3 py-2 border border-gray-300 rounded focus:outline-none focus:border-blue-500" />
    </div>
    <button type="submit" class="w-full bg-blue-500 text-white py-2 rounded hover:bg-blue-700">
        Submit
    </button>
</form>
```

### Tailwind Configuration and Customization

```javascript
// tailwind.config.js
module.exports = {
    content: [
        "./index.html",
        "./src/**/*.{js,ts,jsx,tsx}",
    ],
    theme: {
        extend: {
            colors: {
                primary: '#3b82f6',
                secondary: '#10b981',
                accent: '#f59e0b',
            },
            fontFamily: {
                sans: ['Roboto', 'sans-serif'],
                serif: ['Merriweather', 'serif'],
            },
            spacing: {
                '128': '32rem',
                '144': '36rem',
            },
            borderRadius: {
                'xl': '1rem',
                '2xl': '1.5rem',
            },
        },
    },
    plugins: [
        require('@tailwindcss/forms'),
        require('@tailwindcss/typography'),
    ],
}
```

### Tailwind Best Practices

1. **Use @apply for repeated patterns**: Create reusable component classes
2. **Extract components**: Use Tailwind's component layer for complex components
3. **Use custom utilities**: Extend Tailwind for project-specific needs
4. **Organize classes**: Use consistent ordering (layout, spacing, colors, etc.)
5. **Leverage responsive prefixes**: Build mobile-first designs
6. **Use CSS variables**: Combine with Tailwind for dynamic theming
7. **Optimize production**: Tailwind automatically purges unused styles

---

## Next.js - Full-Stack React Framework {#nextjs}

### Introduction to Next.js

Next.js is a React framework for building full-stack web applications with features like server-side rendering, static site generation, API routes, and more. It provides a complete development environment with built-in optimization and deployment capabilities.

### Installation and Setup

```bash
# Create new Next.js project
npx create-next-app@latest my-app

# Navigate to project
cd my-app

# Run development server
npm run dev
```

### File-Based Routing

Next.js uses file-based routing where the file structure determines the routes:

```
app/
├── page.js                 # / route
├── about/
│   └── page.js            # /about route
├── blog/
│   ├── page.js            # /blog route
│   └── [id]/
│       └── page.js        # /blog/[id] dynamic route
└── api/
    └── users/
        └── route.js       # API endpoint /api/users
```

### Pages and Layouts

**Page Component:**
```jsx
// app/page.js
export default function Home() {
    return (
        <main>
            <h1>Welcome to Next.js</h1>
            <p>This is the home page</p>
        </main>
    );
}
```

**Layout Component:**
```jsx
// app/layout.js
export const metadata = {
    title: 'My App',
    description: 'Generated by create next app',
};

export default function RootLayout({ children }) {
    return (
        <html lang="en">
            <body>
                <header>
                    <nav>
                        <a href="/">Home</a>
                        <a href="/about">About</a>
                    </nav>
                </header>
                <main>{children}</main>
                <footer>
                    <p>&copy; 2025 My App</p>
                </footer>
            </body>
        </html>
    );
}
```

### Dynamic Routes

```jsx
// app/blog/[id]/page.js
export default function BlogPost({ params }) {
    return (
        <article>
            <h1>Blog Post {params.id}</h1>
            <p>Content for post {params.id}</p>
        </article>
    );
}

// Catch-all routes
// app/docs/[[...slug]]/page.js
export default function Docs({ params }) {
    return (
        <div>
            <h1>Documentation</h1>
            <p>Path: {params.slug?.join('/')}</p>
        </div>
    );
}
```

### Server Components and Client Components

**Server Component (default):**
```jsx
// app/users/page.js
async function getUsers() {
    const response = await fetch('https://api.example.com/users');
    return response.json();
}

export default async function UsersPage() {
    const users = await getUsers();
    
    return (
        <div>
            <h1>Users</h1>
            <ul>
                {users.map(user => (
                    <li key={user.id}>{user.name}</li>
                ))}
            </ul>
        </div>
    );
}
```

**Client Component:**
```jsx
// app/counter/page.js
'use client';

import { useState } from 'react';

export default function Counter() {
    const [count, setCount] = useState(0);
    
    return (
        <div>
            <p>Count: {count}</p>
            <button onClick={() => setCount(count + 1)}>
                Increment
            </button>
        </div>
    );
}
```

### Data Fetching

**Server-Side Data Fetching:**
```jsx
// app/posts/page.js
async function getPosts() {
    const response = await fetch('https://api.example.com/posts', {
        next: { revalidate: 60 } // Revalidate every 60 seconds (ISR)
    });
    return response.json();
}

export default async function PostsPage() {
    const posts = await getPosts();
    
    return (
        <div>
            <h1>Posts</h1>
            {posts.map(post => (
                <article key={post.id}>
                    <h2>{post.title}</h2>
                    <p>{post.content}</p>
                </article>
            ))}
        </div>
    );
}
```

**Client-Side Data Fetching with useEffect:**
```jsx
'use client';

import { useState, useEffect } from 'react';

export default function UsersList() {
    const [users, setUsers] = useState([]);
    const [loading, setLoading] = useState(true);
    
    useEffect(() => {
        async function fetchUsers() {
            try {
                const response = await fetch('/api/users');
                const data = await response.json();
                setUsers(data);
            } finally {
                setLoading(false);
            }
        }
        
        fetchUsers();
    }, []);
    
    if (loading) return <div>Loading...</div>;
    
    return (
        <ul>
            {users.map(user => (
                <li key={user.id}>{user.name}</li>
            ))}
        </ul>
    );
}
```

### API Routes

```javascript
// app/api/users/route.js
export async function GET(request) {
    return Response.json([
        { id: 1, name: 'John' },
        { id: 2, name: 'Jane' }
    ]);
}

export async function POST(request) {
    const data = await request.json();
    
    // Process data
    return Response.json(
        { message: 'User created', data },
        { status: 201 }
    );
}

// Dynamic API route
// app/api/users/[id]/route.js
export async function GET(request, { params }) {
    const userId = params.id;
    
    return Response.json({
        id: userId,
        name: 'John',
        email: 'john@example.com'
    });
}

export async function PUT(request, { params }) {
    const userId = params.id;
    const data = await request.json();
    
    return Response.json({
        message: `User ${userId} updated`,
        data
    });
}

export async function DELETE(request, { params }) {
    const userId = params.id;
    
    return Response.json({
        message: `User ${userId} deleted`
    });
}
```

### Middleware

```javascript
// middleware.js
import { NextResponse } from 'next/server';

export function middleware(request) {
    // Check if user is authenticated
    const token = request.cookies.get('token');
    
    if (!token && request.nextUrl.pathname.startsWith('/dashboard')) {
        return NextResponse.redirect(new URL('/login', request.url));
    }
    
    return NextResponse.next();
}

export const config = {
    matcher: ['/dashboard/:path*', '/admin/:path*'],
};
```

### Static Generation and ISR

**Static Generation:**
```jsx
// app/blog/[id]/page.js
export async function generateStaticParams() {
    const posts = await fetch('https://api.example.com/posts').then(res => res.json());
    
    return posts.map(post => ({
        id: post.id.toString(),
    }));
}

export default async function BlogPost({ params }) {
    const post = await fetch(`https://api.example.com/posts/${params.id}`).then(res => res.json());
    
    return (
        <article>
            <h1>{post.title}</h1>
            <p>{post.content}</p>
        </article>
    );
}
```

**Incremental Static Regeneration (ISR):**
```jsx
// app/products/[id]/page.js
export const revalidate = 60; // Revalidate every 60 seconds

async function getProduct(id) {
    const response = await fetch(`https://api.example.com/products/${id}`);
    return response.json();
}

export default async function ProductPage({ params }) {
    const product = await getProduct(params.id);
    
    return (
        <div>
            <h1>{product.name}</h1>
            <p>${product.price}</p>
        </div>
    );
}
```

### Image Optimization

```jsx
import Image from 'next/image';

export default function Hero() {
    return (
        <Image
            src="/hero.jpg"
            alt="Hero image"
            width={1200}
            height={600}
            priority
        />
    );
}
```

### Deployment

**Deploy to Vercel:**
```bash
# Install Vercel CLI
npm i -g vercel

# Deploy
vercel
```

**Environment Variables:**
```bash
# .env.local
DATABASE_URL=postgresql://...
API_KEY=your-api-key

# .env.production
DATABASE_URL=postgresql://...
API_KEY=production-api-key
```

### Next.js Best Practices

1. **Use Server Components**: Default to server components for better performance
2. **Optimize Images**: Use Next.js Image component for automatic optimization
3. **Implement ISR**: Use revalidate for dynamic content that changes infrequently
4. **Use API Routes**: Build backend functionality within Next.js
5. **Environment Variables**: Secure sensitive data with environment variables
6. **Code Splitting**: Next.js automatically splits code by route
7. **SEO Optimization**: Use metadata API for SEO
8. **Performance Monitoring**: Use Web Vitals for performance tracking

---

## References {#references}

1. [MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
2. [W3C HTML Specification](https://html.spec.whatwg.org/)
3. [MDN Web Docs - CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
4. [CSS Tricks - Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
5. [CSS Tricks - Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
6. [Bootstrap Official Documentation](https://getbootstrap.com/docs/)
7. [MDN Web Docs - JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
8. [JavaScript.info - Complete JavaScript Tutorial](https://javascript.info/)
9. [React Official Documentation](https://react.dev/)
10. [React Hooks Documentation](https://react.dev/reference/react/hooks)
11. [Tailwind CSS Official Documentation](https://tailwindcss.com/docs)
12. [Next.js Official Documentation](https://nextjs.org/docs)
13. [Next.js App Router Documentation](https://nextjs.org/docs/app)
14. [MDN Web Docs - Web Accessibility](https://developer.mozilla.org/en-US/docs/Web/Accessibility)
15. [Web.dev - Web Performance](https://web.dev/performance/)

---

### What is Git?
- Distributed version control system for tracking changes in source code during software development.
- Facilitates collaboration among developers.

### Essential Git Commands
- `git init`: Initialize a new Git repository.
- `git add .`: Stage changes for commit.
- `git commit -m "Message"`: Save staged changes to history.
- `git status`: Check the status of your working directory.
- `git push`: Upload local repository content to a remote repository.
- `git pull`: Fetch and download content from a remote repository and immediately update the local repository to match that content.

### Practical Example: Basic Workflow
```bash
git init
echo "Hello World" > index.html
git add index.html
git commit -m "Initial commit: Add index.html"
```

## Slide 10: GitHub - Collaboration and Hosting

### What is GitHub?
- Web-based platform for version control and collaboration using Git.
- Provides hosting for software development and distributed version control.

This comprehensive guide covers the fundamental concepts, practical examples, and best practices for front-end development technologies. Each section includes detailed explanations, code examples, and best practices to help developers master these essential tools for building modern web applications.

