<!--

@license Apache-2.0

Copyright (c) 2025 The Stdlib Authors.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

-->


<details>
  <summary>
    About stdlib...
  </summary>
  <p>We believe in a future in which the web is a preferred environment for numerical computation. To help realize this future, we've built stdlib. stdlib is a standard library, with an emphasis on numerical and scientific computation, written in JavaScript (and C) for execution in browsers and in Node.js.</p>
  <p>The library is fully decomposable, being architected in such a way that you can swap out and mix and match APIs and functionality to cater to your exact preferences and use cases.</p>
  <p>When you use stdlib, you can be absolutely certain that you are using the most thorough, rigorous, well-written, studied, documented, tested, measured, and high-quality code out there.</p>
  <p>To join us in bringing numerical computing to the web, get started by checking us out on <a href="https://github.com/stdlib-js/stdlib">GitHub</a>, and please consider <a href="https://opencollective.com/stdlib">financially supporting stdlib</a>. We greatly appreciate your continued support!</p>
</details>

# Bradford

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] <!-- [![dependencies][dependencies-image]][dependencies-url] -->

> Bradford distribution.



<section class="usage">

## Usage

To use in Observable,

```javascript
bradford = require( 'https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-bradford@umd/browser.js' )
```

To vendor stdlib functionality and avoid installing dependency trees for Node.js, you can use the UMD server build:

```javascript
var bradford = require( 'path/to/vendor/umd/stats-base-dists-bradford/index.js' )
```

To include the bundle in a webpage,

```html
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-bradford@umd/browser.js"></script>
```

If no recognized module system is present, access bundle contents via the global scope:

```html
<script type="text/javascript">
(function () {
    window.bradford;
})();
</script>
```

#### bradford

[Bradford][bradford-distribution] distribution.

```javascript
var dist = bradford;
// returns {...}
```

The namespace contains the following distribution functions:

<!-- <toc pattern="*+(cdf|pdf|mgf|quantile)*"> -->

<div class="namespace-toc">

-   <span class="signature">[`cdf( x, c )`][@stdlib/stats/base/dists/bradford/cdf]</span><span class="delimiter">: </span><span class="description">bradford distribution cumulative distribution function (CDF).</span>
-   <span class="signature">[`pdf( x, c )`][@stdlib/stats/base/dists/bradford/pdf]</span><span class="delimiter">: </span><span class="description">bradford distribution probability density function (PDF).</span>
-   <span class="signature">[`quantile( p, c )`][@stdlib/stats/base/dists/bradford/quantile]</span><span class="delimiter">: </span><span class="description">bradford distribution quantile function.</span>

</div>

<!-- </toc> -->

The namespace contains the following functions for calculating distribution properties:

<!-- <toc pattern="*+(entropy|mean|median|mode|skewness|stdev|variance)*"> -->

<div class="namespace-toc">

-   <span class="signature">[`entropy( c )`][@stdlib/stats/base/dists/bradford/entropy]</span><span class="delimiter">: </span><span class="description">bradford distribution differential entropy.</span>
-   <span class="signature">[`mean( c )`][@stdlib/stats/base/dists/bradford/mean]</span><span class="delimiter">: </span><span class="description">bradford distribution expected value.</span>
-   <span class="signature">[`median( c )`][@stdlib/stats/base/dists/bradford/median]</span><span class="delimiter">: </span><span class="description">bradford distribution median.</span>
-   <span class="signature">[`mode( c )`][@stdlib/stats/base/dists/bradford/mode]</span><span class="delimiter">: </span><span class="description">bradford distribution mode.</span>
-   <span class="signature">[`skewness( c )`][@stdlib/stats/base/dists/bradford/skewness]</span><span class="delimiter">: </span><span class="description">bradford distribution skewness.</span>
-   <span class="signature">[`stdev( c )`][@stdlib/stats/base/dists/bradford/stdev]</span><span class="delimiter">: </span><span class="description">bradford distribution standard deviation.</span>
-   <span class="signature">[`variance( c )`][@stdlib/stats/base/dists/bradford/variance]</span><span class="delimiter">: </span><span class="description">bradford distribution variance.</span>

</div>

<!-- </toc> -->

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint no-undef: "error" -->

```html
<!DOCTYPE html>
<html lang="en">
<body>
<script type="text/javascript" src="https://cdn.jsdelivr.net/gh/stdlib-js/stats-base-dists-bradford@umd/browser.js"></script>
<script type="text/javascript">
(function () {

/*
* The Bradford distribution is defined over [0,1] with shape parameter c.
*/

var c = 2.0;

// Compute the mean:
var mu = bradford.mean( c );
// returns ~0.410

// Compute the median:
var median = bradford.median( c );
// returns ~0.366

// Compute the variance:
var s2 = bradford.variance( c );
// returns ~0.082

// Compute the standard deviation:
var sigma = bradford.stdev( c );
// returns ~0.286

// Evaluate the PDF at x = 0.5:
var y = bradford.pdf( 0.5, c );
// returns ~0.910

// Evaluate the CDF at x = 0.5:
var p = bradford.cdf( 0.5, c );
// returns ~0.631

// Compute the 50th percentile (median):
var q = bradford.quantile( 0.5, c );
// returns ~0.366

// Compute the entropy:
var h = bradford.entropy( c );
// returns ~-0.050

// Compute the skewness:
var skew = bradford.skewness( c );
// returns ~0.378

// Compute the mode:
var mode = bradford.mode( c );
// returns 0.0

})();
</script>
</body>
</html>
```

</section>

<!-- /.examples -->

<!-- Section for related `stdlib` packages. Do not manually edit this section, as it is automatically populated. -->

<section class="related">

</section>

<!-- /.related -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->


<section class="main-repo" >

* * *

## Notice

This package is part of [stdlib][stdlib], a standard library for JavaScript and Node.js, with an emphasis on numerical and scientific computing. The library provides a collection of robust, high performance libraries for mathematics, statistics, streams, utilities, and more.

For more information on the project, filing bug reports and feature requests, and guidance on how to develop [stdlib][stdlib], see the main project [repository][stdlib].

#### Community

[![Chat][chat-image]][chat-url]

---

## License

See [LICENSE][stdlib-license].


## Copyright

Copyright &copy; 2016-2026. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/stats-base-dists-bradford.svg
[npm-url]: https://npmjs.org/package/@stdlib/stats-base-dists-bradford

[test-image]: https://github.com/stdlib-js/stats-base-dists-bradford/actions/workflows/test.yml/badge.svg?branch=v0.1.0
[test-url]: https://github.com/stdlib-js/stats-base-dists-bradford/actions/workflows/test.yml?query=branch:v0.1.0

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/stats-base-dists-bradford/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/stats-base-dists-bradford?branch=main

<!--

[dependencies-image]: https://img.shields.io/david/stdlib-js/stats-base-dists-bradford.svg
[dependencies-url]: https://david-dm.org/stdlib-js/stats-base-dists-bradford/main

-->

[chat-image]: https://img.shields.io/badge/zulip-join_chat-brightgreen.svg
[chat-url]: https://stdlib.zulipchat.com

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[umd]: https://github.com/umdjs/umd
[es-module]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Modules

[deno-url]: https://github.com/stdlib-js/stats-base-dists-bradford/tree/deno
[deno-readme]: https://github.com/stdlib-js/stats-base-dists-bradford/blob/deno/README.md
[umd-url]: https://github.com/stdlib-js/stats-base-dists-bradford/tree/umd
[umd-readme]: https://github.com/stdlib-js/stats-base-dists-bradford/blob/umd/README.md
[esm-url]: https://github.com/stdlib-js/stats-base-dists-bradford/tree/esm
[esm-readme]: https://github.com/stdlib-js/stats-base-dists-bradford/blob/esm/README.md
[branches-url]: https://github.com/stdlib-js/stats-base-dists-bradford/blob/main/branches.md

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/stats-base-dists-bradford/main/LICENSE

[bradford-distribution]: https://en.wikipedia.org/wiki/Bradford_distribution

<!-- <toc-links> -->

[@stdlib/stats/base/dists/bradford/entropy]: https://github.com/stdlib-js/stats-base-dists-bradford-entropy/tree/umd

[@stdlib/stats/base/dists/bradford/mean]: https://github.com/stdlib-js/stats-base-dists-bradford-mean/tree/umd

[@stdlib/stats/base/dists/bradford/median]: https://github.com/stdlib-js/stats-base-dists-bradford-median/tree/umd

[@stdlib/stats/base/dists/bradford/mode]: https://github.com/stdlib-js/stats-base-dists-bradford-mode/tree/umd

[@stdlib/stats/base/dists/bradford/skewness]: https://github.com/stdlib-js/stats-base-dists-bradford-skewness/tree/umd

[@stdlib/stats/base/dists/bradford/stdev]: https://github.com/stdlib-js/stats-base-dists-bradford-stdev/tree/umd

[@stdlib/stats/base/dists/bradford/variance]: https://github.com/stdlib-js/stats-base-dists-bradford-variance/tree/umd

[@stdlib/stats/base/dists/bradford/cdf]: https://github.com/stdlib-js/stats-base-dists-bradford-cdf/tree/umd

[@stdlib/stats/base/dists/bradford/pdf]: https://github.com/stdlib-js/stats-base-dists-bradford-pdf/tree/umd

[@stdlib/stats/base/dists/bradford/quantile]: https://github.com/stdlib-js/stats-base-dists-bradford-quantile/tree/umd

<!-- </toc-links> -->

</section>

<!-- /.links -->
