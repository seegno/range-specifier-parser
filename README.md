# Range Specifier Parser

A parser to handle [Range Pagination Headers](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html).

*Inspired by [range-parser](https://github.com/jshttp/range-parser)*.

## Installation

Choose your preferred method:

* npm: `npm install --save range-specifier-parser`
* Download: [range-specifier-parser](https://github.com/seegno/range-specifier-parser)

## Usage

The parser receives a `byte-ranges-specifier` as its only argument.

```js
var parser = require('range-specifier-parser');

parser('bytes=0-499');

```

## Output

The parser outputs an object with the following properties according to the [Byte Ranges](http://www.w3.org/Protocols/rfc2616/rfc2616-sec14.html#sec14.35.1) spec:


```js
{
  first: 0, // `first-byte-pos`.
  last: 499, // `last-byte-pos`.
  unit: 'bytes' // `bytes-unit`.
}

```

## Running tests

```sh
npm test
```
