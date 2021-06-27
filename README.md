<!--

@license Apache-2.0

Copyright (c) 2018 The Stdlib Authors.

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

# isNegativeIntegerArray

[![NPM version][npm-image]][npm-url] [![Build Status][test-image]][test-url] [![Coverage Status][coverage-image]][coverage-url] [![dependencies][dependencies-image]][dependencies-url]

> Test if a value is an array-like object containing only negative integers.

<section class="installation">

## Installation

```bash
npm install @stdlib/assert-is-negative-integer-array
```

</section>

<section class="usage">

## Usage

```javascript
var isNegativeIntegerArray = require( '@stdlib/assert-is-negative-integer-array' );
```

#### isNegativeIntegerArray( value )

Tests if a `value` is an array-like object containing **only** negative `integer` values.

<!-- eslint-disable no-new-wrappers -->

```javascript
var Number = require( '@stdlib/number-ctor' );

var bool = isNegativeIntegerArray( [ -3, new Number(-3) ] );
// returns true

bool = isNegativeIntegerArray( [ -3, '3.0' ] );
// returns false
```

#### isNegativeIntegerArray.primitives( value )

Tests if a `value` is an array-like object containing **only** negative primitive `integer` values.

<!-- eslint-disable no-new-wrappers -->

```javascript
var Number = require( '@stdlib/number-ctor' );

var bool = isNegativeIntegerArray.primitives( [ -1.0, -10.0 ] );
// returns true

bool = isNegativeIntegerArray.primitives( [ -1.0, 0.0, -10.0 ] );
// returns false

bool = isNegativeIntegerArray.primitives( [ -3.0, new Number(-1.0) ] );
// returns false
```

#### isNegativeIntegerArray.objects( value )

Tests if a `value` is an array-like object containing **only** `Number` objects holding negative `integer` values.

<!-- eslint-disable no-new-wrappers, max-len -->

```javascript
var Number = require( '@stdlib/number-ctor' );

var bool = isNegativeIntegerArray.objects( [ new Number(-1.0), new Number(-10.0) ] );
// returns true

bool = isNegativeIntegerArray.objects( [ -1.0, 0.0, -10.0 ] );
// returns false

bool = isNegativeIntegerArray.objects( [ -3.0, new Number(-1.0) ] );
// returns false
```

</section>

<!-- /.usage -->

<section class="examples">

## Examples

<!-- eslint-disable no-new-wrappers -->

<!-- eslint no-undef: "error" -->

```javascript
var Number = require( '@stdlib/number-ctor' );
var isNegativeIntegerArray = require( '@stdlib/assert-is-negative-integer-array' );

var bool = isNegativeIntegerArray( [ -5, -2, -3 ] );
// returns true

bool = isNegativeIntegerArray( [ -4, -3, -2, -1 ] );
// returns true

bool = isNegativeIntegerArray( [ -1, new Number( -6 ), -3 ] );
// returns true

bool = isNegativeIntegerArray( [ -3, -2, -1, 0 ] );
// returns false

bool = isNegativeIntegerArray( [ -1, 'abc', -3 ] );
// returns false

bool = isNegativeIntegerArray( [ -2.3, -1, -3 ] );
// returns false

bool = isNegativeIntegerArray( [] );
// returns false
```

</section>

<!-- /.examples -->


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

Copyright &copy; 2016-2021. The Stdlib [Authors][stdlib-authors].

</section>

<!-- /.stdlib -->

<!-- Section for all links. Make sure to keep an empty line after the `section` element and another before the `/section` close. -->

<section class="links">

[npm-image]: http://img.shields.io/npm/v/@stdlib/assert-is-negative-integer-array.svg
[npm-url]: https://npmjs.org/package/@stdlib/assert-is-negative-integer-array

[test-image]: https://github.com/stdlib-js/assert-is-negative-integer-array/actions/workflows/test.yml/badge.svg
[test-url]: https://github.com/stdlib-js/assert-is-negative-integer-array/actions/workflows/test.yml

[coverage-image]: https://img.shields.io/codecov/c/github/stdlib-js/assert-is-negative-integer-array/main.svg
[coverage-url]: https://codecov.io/github/stdlib-js/assert-is-negative-integer-array?branch=main

[dependencies-image]: https://img.shields.io/david/stdlib-js/assert-is-negative-integer-array.svg
[dependencies-url]: https://david-dm.org/stdlib-js/assert-is-negative-integer-array/main

[chat-image]: https://img.shields.io/gitter/room/stdlib-js/stdlib.svg
[chat-url]: https://gitter.im/stdlib-js/stdlib/

[stdlib]: https://github.com/stdlib-js/stdlib

[stdlib-authors]: https://github.com/stdlib-js/stdlib/graphs/contributors

[stdlib-license]: https://raw.githubusercontent.com/stdlib-js/assert-is-negative-integer-array/main/LICENSE

</section>

<!-- /.links -->