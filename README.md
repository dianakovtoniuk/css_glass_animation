# Colorful Liquid Glass Animation

A liquid-in-a-glass animation built with pure HTML and CSS, no JavaScript. Created as practice with CSS keyframes and pseudo-elements.

## Preview

Two glasses stand side by side on a dark background, one filled with blue liquid and the other with yellow. The liquid level slowly drops and rises again, and the second glass runs half a cycle behind the first.

## How it works

- Each glass is built from nested elements: `.glass`, `.inner` and `.liquid`.
- The rim of the glass is drawn with the `.inner::before` pseudo-element, and the light reflection on the side with `.inner::after`.
- The liquid is an absolutely positioned block. Its surface is a darker ellipse made with `.liquid::before` and `border-radius: 50%`.
- A single `@keyframes` animation moves the liquid by changing its `top` value, with short pauses at the top and bottom of the cycle.
- The second glass uses a different color and a 2.5s `animation-delay`, so the two levels move in opposite phases.

## Usage

Clone or download the repo and open `index.html` in a browser.

```
colorful-liquid-glass-animation/
├── index.html
└── style.css
```

## Customization

In `style.css` you can tweak:

- `animation` duration on `.liquid` to change the speed
- `top` values in `@keyframes animateLiquid` to change how far the level drops
- `background` on `.liquid` and `.liquid::before` to change the liquid and surface colors
- `width` and `height` on `.glass .inner` to resize the glasses
- the number of `.glass` elements in the HTML, with its own color and `animation-delay` for each new one
