parse-cube-lut
==============
### Cube LUT (IRIDAS/Adobe) parser

Parses Cube LUT files as defined in the [Adobe specification](http://wwwimages.adobe.com/content/dam/Adobe/en/products/speedgrade/cc/pdfs/cube-lut-specification-1.0.pdf).

LUT files are useful for color grading, encapsulating complex color-space transforms or emulating film stock for photography and video.

Install
-------

```bash
$ npm install parse-cube-lut
```

Usage
-----

```javascript
var parseCubeLUT = require('parse-cube-lut');
var fs = require('fs');

var buf = fs.readFileSync('fuji400h.cube');
var lut = parseCubeLUT(buf);

console.log(lut);
/*
{ title: 'Fuji 400H LUT',
  type: '3D',
  size: 25,
  domain: [ [ 0, 0, 0 ], [ 1, 1, 1 ] ],
  data: [
    [0, 0, 0],
    ...
  ]
}
*/
```