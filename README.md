# [Flex Panel Image Gallery](http://travis.bingo/flexPanels/)
Image gallery app with Flexbox and CSS transitions. Click panels for animation.

* Nested Flex containers
* Animating (transitioning) the flex property
* Animating with cubic-bezier
* Timing sequence in animation effects with the `transitionend` event
* `e.propertyName.includes()`

# Toggling classes with JavaScript `click` and `transitionend` events

```js
const panels = document.querySelectorAll('.panel');

panels.forEach(panel => panel.addEventListener('click', toggleOpen));
panels.forEach(panel => panel.addEventListener('transitionend', toggleActive));

function toggleActive(e) {
  if (e.propertyName.includes('flex')) {
    this.classList.toggle('open-active');
  }
}

function toggleOpen() {
  this.classList.toggle('open');
}

```
