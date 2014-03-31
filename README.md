# RGB K-means clustering
A js RGB [K-means clustering](http://en.wikipedia.org/wiki/K-means_clusteri) library.

# Install

For seajs:

```bash
spm install rgbkmeans
```

# K-means

```javascript
var kmeans = require("kmeans");

var colors = [
   [20, 20, 80],
   [22, 22, 90],
   [250, 255, 253],
   [0, 30, 70],
   [200, 0, 23],
   [100, 54, 100],
   [255, 13, 8]
];

var clusters = kmeans(colors, 3);
```

The second argument to `kmeans` is the number of clusters you want (default is `Math.sqrt(n/2)` where `n` is the number of vectors). It returns an array of the clusters, for this example:

```javascript
[
  [[200,0,23], [255,13,8]],
  [[20,20,80], [22,22,90], [0,30,70], [100,54,100]],
  [[250,255,253]]
]
```

#### Distance metric

Specify the distance metric, one of `"euclidean"` (default), `"manhattan"`, and `"max"`.

```javascript
var clusters = kmeans(colors, "euclidean");
```
