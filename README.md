# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements
- View a product card with an image, product details, pricing information, and an "Add to Cart" button


### Screenshot

#### Desktop View
![Desktop Design](./design/desktop-design.jpg)

#### Mobile View
![Mobile Design](./design/mobile-design.jpg)

#### Active Status
![Mobile Design](./design/active-states.jpg)

### Links

- Solution URL: [GitHub Repository](https://github.com/yourusername/product-preview-card-component)
- Live Site URL: [Live Demo](https://yourusername.github.io/product-preview-card-component)

## My process

### Built with

- Semantic HTML5 markup
- CSS with flexible units (rem/em)
- Flexbox for layout and alignment
- Mobile-first responsive workflow
- Responsive Media Queries (Mobile: 375px, Desktop: 1440px+)
- Google Fonts (Montserrat & Fraunces)

### What I learned

This project was a great opportunity to practice several key frontend concepts:

**1. Semantic HTML Structure**
```html
<picture>
  <source media="(min-width: 768px)" srcset="images/image-product-desktop.jpg">
  <img src="images/image-product-mobile.jpg" alt="product">
</picture>
```
I learned how to use the `<picture>` element to serve different images based on screen size, improving performance and responsive design.

**2. Flexible Units (rem/em) Over Pixels**
One of the most important learnings was converting all fixed pixel values to relative rem units:
```css
/* Before */
.card {
  padding: 20px;
  border-radius: 10px;
  font-size: 14px;
}

/* After */
.card {
  padding: 1.25rem;
  border-radius: 0.625rem;
  font-size: 0.875rem;
}
```
Using rem units makes the design more accessible because it respects user's browser font size preferences and makes scaling across breakpoints much easier.

**3. Flexbox for Centering and Alignment**
```css
body {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}

.card__content__price {
  display: flex;
  align-items: center;
  gap: 1.25rem;
}
```
Flexbox simplified complex alignment tasks and made the layout responsive without extra media queries.

**4. Mobile-First Responsive Design**
I learned to design for mobile first, then enhance the layout for larger screens:
```css
@media (min-width: 48rem) { /* 768px */
  .card {
    display: flex;
    max-width: 37.5rem;
  }
}
```

**5. CSS Custom Properties for Maintainability**
Styling a card component with clear class naming conventions made the code more maintainable and scalable.

### Continued development

Areas I want to continue exploring:

- **CSS Custom Properties (Variables)** - Using `--color-primary` and `--spacing-base` to make theming easier
- **Advanced Responsive Patterns** - Exploring CSS Grid for more complex layouts
- **Accessibility (a11y)** - Adding ARIA labels and improving keyboard navigation
- **JavaScript Interactivity** - Adding hover effects and interactive states dynamically
- **Performance Optimization** - Learning WebP image formats and lazy loading

### Useful resources

- [MDN Web Docs - Flexbox](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout) - Clear explanations of flexbox properties with visual examples
- [MDN Web Docs - rem Units](https://developer.mozilla.org/en-US/docs/Learn/CSS/Building_blocks/Values_and_units#ems_and_rems) - Understanding relative sizing units
- [Frontend Mentor - Learning Paths](https://www.frontendmentor.io/learning-paths) - Structured learning resources for beginners
- [CSS-Tricks - A Complete Guide to Flexbox](https://css-tricks.com/snippets/css/a-guide-to-flexbox/) - Visual guide to flexbox properties
- [Google Fonts](https://fonts.google.com/) - Free fonts used in this project (Montserrat & Fraunces)

### AI Collaboration

I used GitHub Copilot to help with this project:

- **Code Structure Guidance** - Helped organize semantic HTML and CSS class naming conventions
- **Conversion to rem Units** - Assisted in calculating and converting all pixel values to rem for better accessibility and scalability
- **Responsive Design** - Provided guidance on media query breakpoints and responsive patterns
- **What Worked Well** - Copilot was particularly helpful for understanding the reasoning behind flexible units and mobile-first development

## Author

- GitHub - [Mohamed Hodaib](https://github.com/mohamedHodaib)
- Frontend Mentor - [@mohamedHodaib](https://www.frontendmentor.io/profile/mohamedHodaib)
- LinkedIn - [Mohamed Hodaib](https://www.linkedin.com/in/mohamed-hodaib-2670b2344/)
