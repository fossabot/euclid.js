# Euclid.ts

[![Build Status](https://travis-ci.org/mathigon/euclid.js.svg?branch=master)](https://travis-ci.org/mathigon/euclid.js)
[![npm](https://img.shields.io/npm/v/@mathigon/euclid.svg)](https://www.npmjs.com/package/@mathigon/euclid)
[![npm](https://img.shields.io/github/license/mathigon/euclid.js.svg)](https://github.com/mathigon/euclid.js/blob/master/LICENSE)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fmathigon%2Feuclid.js.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2Fmathigon%2Feuclid.js?ref=badge_shield)

Euclid.ts is a Typescript library for 2D geometry. It contains classes for elements like points,
lines, circles, and polygons, intersection detection, as well as SVG and Canvas drawing tools.
It was developed for [Mathigon.org](https://mathigon.org), an award-winning mathematics education
project.


## API

All class instances are immutable: you need to create new copies rather than modifying their
properties. This is mainly to facilitate fast change detection on downstream libraries.

* Points: `Point(x: number, y: number)`
* Lines: `Line(p1: Point, p2: Point)`, `Segment(p1: Point, p2: Point)`, `Ray(p1: Point, p2: Point)`
* Polygons: `Polygon(...points: Point[])`, `Polyline(...points: Point[])`
* Rectangles: `Rectangle(p: Point, w: number, h: number)`
* Circles: `Circle(c: Point, r: number)`
* Ellipses: `Ellipse(c: Point, a: number, b: number)` 
* Arcs: `Arc((c: Point, start: Point, angle: number))`, `Sector((c: Point, start: Point, angle: number))`

* Angle: `Angle(a: Point, b: Point, c: Point)`
* Bounds: `Bounds(xMin: number, xMax: number, yMin: number, yMax: number)`

* Intersections: `intsersection(...obj: GeoShape[])`
* Drawing: `drawSVG(obj: GeoElement, options: SVGDrawingOptions)`, `drawCanvas(ctx: CanvasRenderingContext2D, obj: GeoElement, options: CanvasDrawingOptions)`


## Usage

First, install Euclid.ts from [NPM](https://www.npmjs.com/package/@mathigon/euclid)
using

```npm install @mathigon/euclid```

Now, simply import all functions and classes you need, using

```js
import {Point, Line} from '@mathigon/euclid'
```


## Contributing

We welcome community contributions: please file any bugs you find or send us
pull requests with improvements. You can find out more on
[Mathigon.io](https://mathigon.io).

Before submitting a pull request, you will need to sign the [Mathigon Individual
Contributor License Agreement](https://gist.github.com/plegner/5ad5b7be2948a4ad073c50b15ac01d39).


## Copyright and License

Copyright © Mathigon ([dev@mathigon.org](mailto:dev@mathigon.org))  
Released under the [MIT license](LICENSE)


[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fmathigon%2Feuclid.js.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fmathigon%2Feuclid.js?ref=badge_large)