# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

Blog card component, includes main photo, tag, date, title, short description, and author information (including: name and avatar).

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page

### Screenshot

![](./preview.jpg)

### Links

- Solution URL: [GitHub](https://github.com/jmmarketing/blog-preview-card-FEM)
- Live Site URL: [LIVE](https://jmmarketing.github.io/blog-preview-card-FEM/)

## My process

- Check provided direction, designs, files, etc..
- Lay out project folder structure (SCSS/SASS)
- Build general structure (HTML) using BEM naming convention.
- Start with default values for \*, body, html.
- Add necessary files for SCSS.
- I like to build desktop first and then scale down. I grew up with looking at Desktop and then Mobile coming later. It makes sense to me, but I understand how younger developers who started a phone first find mobile easier.
- Create breakpoints (based of specified design) with Mixins.
- Build, check, edit.

### Built with

- Semantic HTML5 markup
- CSS via SCSS
- Flex

### What I learned

Learned that even with flex, sometimes it is quicker to get a solution working and going back to tweak it later.

In this project, I was having a problem with the attribution positioned at the bottom of the page. Flex worked for about 90% of it, but had to give attribute element an absolute position with a bottom property value. It works, but I think there is a solution that is 100% flex.

```html
<div class="card">
  <img
    src="./assets/images/illustration-article.svg"
    alt="Blog post title"
    class="card__blog-img"
  />
  <div class="card__content-box">
    <h4 class="card__tag">Learning</h4>
    <p class="card__date">Published 21 Dec 2023</p>
    <h3 class="card__title">HTML & CSS foundations</h3>
    <p class="card__excerpt">
      These languages are the backbone of every website, defining structure,
      content, and presentation.
    </p>
  </div>
  <div class="card__author-box">
    <img
      src="./assets/images/image-avatar.webp"
      alt=""
      class="card__author-img"
    />
    <h5 class="card__author">Greg Hooper</h5>
  </div>
</div>
```

```css
.card {
  background-color: $color-white;
  padding: 24px;

  border-radius: 20px;
  border: 1px solid $color-grey--dark;
  box-shadow: 8px 8px 0px 0px black;
  width: clamp(327px, 100%, 384px);

  display: flex;
  flex-direction: column;
  //   align-items: flex-start;
  gap: 24px;

  &__blog-img {
    border-radius: 10px;
    align-self: stretch;
    align-items: center;
  }

  &__content-box {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  &__tag {
    font-size: 1.4rem;
    font-weight: 800;
    padding: 4px 12px;
    background-color: $primary-color-yellow;
    border-radius: 4px;
    width: fit-content;

    @include respond(phone) {
      font-size: 1.2rem;
    }
  }

  &__date {
    font-size: 1.4rem;
    font-weight: 500;

    @include respond(phone) {
      font-size: 1.2rem;
    }
  }

  &__title {
    font-size: 2.4rem;
    font-weight: 800;
    line-height: 150%;
    cursor: pointer;

    @include respond(phone) {
      font-size: 2rem;
    }

    &:hover {
      color: $primary-color-yellow;
    }
  }

  &__excerpt {
    font-size: $defaul-font-size;
    font-weight: 500;
    line-height: 150%;

    @include respond(phone) {
      font-size: 1.4rem;
    }
  }

  &__author-box {
    display: flex;
    align-items: center;
    gap: 12px;
  }

  &__author-img {
    width: 32px;
    height: 32px;
  }

  &__author {
    font-size: 1.4rem;
    font-weight: 800;
  }
}
```

### Continued development

Going to continue using these component challenges to work on SCSS features. I want to get more comfortable with mixins, utilities, and functions.

## Author

- Website - [Jeffrey McLean | Marketing Technology, Automation, Design & Development](https://jeffreymclean.com)
- Frontend Mentor - [@jmmarketing](https://www.frontendmentor.io/profile/jmmarketing)
- Twitter - [@jeffe_mclean](https://www.twitter.com/jeffe_mclean)
