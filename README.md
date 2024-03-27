# Frontend Mentor - Newsletter sign-up form with success message solution

This is a solution to the [Newsletter sign-up form with success message challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/newsletter-signup-form-with-success-message-3FC1AZbNrv). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Newsletter sign-up form with success message solution](#frontend-mentor---newsletter-sign-up-form-with-success-message-solution)
  - [Table of contents](#table-of-contents)
  - [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Screenshot](#screenshot)
    - [Links](#links)
  - [My process](#my-process)
    - [Built with](#built-with)
    - [What I learned](#what-i-learned)
    - [Continued development](#continued-development)
  - [Author](#author)

## Overview

### The challenge

Users should be able to:

- Add their email and submit the form
- See a success message with their email after successfully submitting the form
- See form validation messages if:
  - The field is left empty
  - The email address is not formatted correctly
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![screen-shot](./assets/images/screen-shot.png)

### Links

- Solution URL: [*VIEW CODE*](https://github.com/Phurba-Sherpa/frontend-mentor--newsletter-sign-up)
- Live Site URL: [*PREVIEW SITE*](https://phurba-sherpa.github.io/frontend-mentor--newsletter-sign-up/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow

### What I learned

- When using required attribute in html element, and if you set some styles on `:invalid` then on page load, the invalid styles get applied to avoid this messup you can use css like below:

```css
input:invalid:focus {
  border: 1px solid;
}
```

- Learned a trick to select previous element
Suppose we want to show error message if input is invalid

```html
<div class='input-block'>
  <div class='input__helper-text'>
    <label class='input__lable' htmlFor='email'>Email address*</label>
    <p  hidden class='input__feedback'>Valid input required</p>
  </div>
  <input  id='email' type='email' required placeholder='you@comapny.com' autocomplete="off">
</div>
```

What we want is once the input element is invalid, we want to show the error message. Then we can do by following

```css

.input__feedback {
  dispaly: none;
}

input:invalid:focus {
  border: 1px solid red;
}

.input__helper-text:has(+input:invalid:focus) > .input__feedback {
  dispaly: block;
}
```

### Continued development

I can write html and css code that works fine. But I am really bad at writing semantic html, minimal css and full fledge responsivness. Also not good with animation. Also currently I take a lot of time to build the UI. In future I will want to build more robust UI with tricks of Grid. Also want to be more effective when it comes to the timing.

## Author

- Website - [Phurba Sherpa](https://phurba.sherpa.name.np)
- Frontend Mentor - [@Phurba-Sherpa](https://www.frontendmentor.io/profile/Phurba-Sherpa)
- Medium - [@phurba](https://medium.com/@phurba)

