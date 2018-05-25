# Short and Sweet, Accessible Character Counter

[![License: MIT](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/rikschennink/short-and-sweet/blob/gh-pages/LICENSE)
[![npm version](https://badge.fury.io/js/short-and-sweet.svg)](https://badge.fury.io/js/short-and-sweet)
[![Donate with PayPal](https://img.shields.io/badge/donate-PayPal.me-pink.svg)](https://www.paypal.me/rikschennink/5)

Tested with VoiceOver (Safari 11) & NVDA (FF 60)
- Tells user the amount of space left when the field is focussed
- Updates the user periodically while typing

Play around with the demo at:
https://codepen.io/rikschennink/pen/LmoJYY

## Features

- No dependencies
- Easy setup
- Accessible


## Time to learn ES6?

Short and Sweet is written in ES6.

If you want to learn how to write modern ES6 JavaScript as well, I highly recommend [ES6 for Everyone](http://bit.ly/es6-course) by Wes Bos. 


## Installation

Install from npm:

```
npm install short-and-sweet --save
```

Or download `dist/short-and-sweet.min.js` and include the script on your page like shown below.


## Usage

Run short-and-sweet like shown below and pass an element reference or a querySelector. For best performance include the script just before the closing `</body>` element.

```html
<textarea maxlength="200"></textarea>

<script src="short-and-sweet.min.js"></script>
<script>
shortAndSweet('textarea', {
  counterClassName: 'my-short-and-sweet-counter'
});
</script>
```


The following options are available to pass to the `shortAndSweet` method.

Option             | Default       | Description              
-------------------|---------------|------------------------------------------------
`counterClassName` | `'short-and-sweet-counter'`          | The classname of the counter element
`counterLabel`     | `'{remaining} characters left'`      | The text shown in the counter element, placeholders available are `{remaining}`, `{maxlength}`, `{length}`
`assistDelay`      | `2000`        | The time in milliseconds the assist waits before updating the user with the screenreader user with the current count
`append` | `(el, counter) => { el.parentNode.appendChild(counter); }` | The method used to append the element to the DOM


## Tested

- Modern browsers
- VoiceOver + Safari
- NVDA + Firefox
- IE 10+


## Versioning

Versioning follows [Semver](http://semver.org).

## License

MIT
