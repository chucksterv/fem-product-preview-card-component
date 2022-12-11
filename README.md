# FEM - Product Page

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)

## Overview

### The challenge

- View the optimal layout depending on their device's screen size
- Changing the image displayed depending on the user's screen size
- Grid layout.

### Screenshot

![](./screenshot.png)

### Links

- Solution URL: [https://github.com/chucksterv/fem-product-preview-card-component]
- Live Site URL: [https://product-page.projects.deshand.com/]

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

- Using the picture element and sourcesets to specify which image should be used in the design depending on the screensize.
- More familiarity with pseudoclasses when adding icons to the button.

```html
<picture>
  <source
    media="(min-width:600px)"
    srcset="/images/image-product-desktop.jpg"
  />
  <img src="images/image-product-mobile.jpg" alt="Product Image" />
</picture>
```

```css
.button {
  /* Used in order to add the cart icon in the pseudoclass. Plain text would 
    work without the display style adjustments */
  display: inline-flex;
  align-items: center;
  justify-content: center;
  gap: 0.5rem;

  background-color: var(--color-primary);
  color: var(--color-neutral-200);
  font-weight: var(--fw-bold);
  cursor: pointer;
  border: none;
  border-radius: 0.5rem;
  height: 3rem;
}

.cart-icon::before {
  content: "";
  width: 15px;
  height: 16px;
  background-image: url("images/icon-cart.svg");
}
```

### Continued development

- Gain more experience with CSS Grid.
- Experiment with the Picture element and its various usecases.
