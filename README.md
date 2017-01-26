# sketchpad-mod [![npm version](https://badge.fury.io/js/sketchpad-mod.svg)](http://badge.fury.io/js/sketchpad-mod)
SketchpadMod this is a simple sketchpad project for drawing, saving and recovering picture easily.
[![NPM](https://nodei.co/npm/sketchpad-mod.png?downloads=true)](https://nodei.co/npm/sketchpad-mod/)

## Installation
Use npm:
```
npm install sketchpad-mod --save
```

## Usage

Having a canvas on the DOM:
```html
<canvas id="sketchpad-mod"></canvas>
```
You should simply configure it by instantiating the SketchpadMod:
```js
import SketchpadMod from 'sketchpad-mod';

const sketchpadMod = new SketchpadMod({
  element: '#sketchpad-mod',
  width: 400,
  height: 400
});
```
After that, the API provides a variety of functionalities:
```js
// undo
sketchpadMod.undo();

// redo
sketchpadMod.redo();

// Change color
sketchpadMod.color = '#FF0000';

// Change stroke size
sketchpadMod.penSize = 10;

// Playback each sketchpad stroke (10 ms is the time between each line piece)
sketchpadMod.animate(10);

// Set size for size canvas (one size for width and height)
sketchpadMod.setCanvasSize(100);

// Set size for size canvas (one size for width and height)
sketchpadMod.readOnly = true;

// Recover sketchpad JSON or Object Settings
sketchpadMod.toJSON();
sketchpadMod.toObject();

// By recovering the sketchpad JSON or Object you can then clone the sketchpad by coding:
const settings = sketchpadMod.toObject();
settings.element = '#other-sketchpad-mod';
const otherSketchpadMod = new SketchpadMod(settings);
```
