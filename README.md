# parse-exr

[![npm version](https://img.shields.io/npm/v/parse-exr)](https://www.npmjs.com/package/parse-exr)
[![stability-stable](https://img.shields.io/badge/stability-stable-green.svg)](https://www.npmjs.com/package/parse-exr)
[![npm minzipped size](https://img.shields.io/bundlephobia/minzip/parse-exr)](https://bundlephobia.com/package/parse-exr)
[![dependencies](https://img.shields.io/librariesio/release/npm/parse-exr)](https://github.com/dmnsgn/parse-exr/blob/main/package.json)
[![types](https://img.shields.io/npm/types/parse-exr)](https://github.com/microsoft/TypeScript)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-fa6673.svg)](https://conventionalcommits.org)
[![styled with prettier](https://img.shields.io/badge/styled_with-Prettier-f8bc45.svg?logo=prettier)](https://github.com/prettier/prettier)
[![linted with eslint](https://img.shields.io/badge/linted_with-ES_Lint-4B32C3.svg?logo=eslint)](https://github.com/eslint/eslint)
[![license](https://img.shields.io/github/license/dmnsgn/parse-exr)](https://github.com/dmnsgn/parse-exr/blob/main/LICENSE.md)

EXR file parser. Ported from [Three.js implementation](https://github.com/mrdoob/three.js/blob/dev/examples/jsm/loaders/EXRLoader.js/) without depending on it.

[![paypal](https://img.shields.io/badge/donate-paypal-informational?logo=paypal)](https://paypal.me/dmnsgn)
[![coinbase](https://img.shields.io/badge/donate-coinbase-informational?logo=coinbase)](https://commerce.coinbase.com/checkout/56cbdf28-e323-48d8-9c98-7019e72c97f3)
[![twitter](https://img.shields.io/twitter/follow/dmnsgn?style=social)](https://twitter.com/dmnsgn)

## Installation

```bash
npm install parse-exr
```

## Usage

```js
import parseExr from "parse-exr";

const exrData = await (await fetch(url)).arrayBuffer();

const FloatType = 1015;
// const HalfFloatType = 1016;
const { data, width, height } = parseExr(exrData, FloatType);

// => Use the data
```

## API

<!-- api-start -->

## Functions

<dl>
<dt><a href="#parseExr">parseExr(buffer, [type])</a> ⇒ <code><a href="#EXRData">EXRData</a></code></dt>
<dd><p>Parse a buffer and return EXR data</p>
</dd>
</dl>

## Typedefs

<dl>
<dt><a href="#EXRData">EXRData</a></dt>
<dd></dd>
</dl>

<a name="parseExr"></a>

## parseExr(buffer, [type]) ⇒ [<code>EXRData</code>](#EXRData)

Parse a buffer and return EXR data

**Kind**: global function

| Param  | Type                                   | Default           | Description                       |
| ------ | -------------------------------------- | ----------------- | --------------------------------- |
| buffer | <code>ArrayBuffer</code>               |                   |                                   |
| [type] | <code>1015</code> \| <code>1016</code> | <code>1016</code> | Float (1015) or Half Float (1016) |

<a name="EXRData"></a>

## EXRData

**Kind**: global typedef
**Properties**

| Name       | Type                                                  |
| ---------- | ----------------------------------------------------- |
| header     | <code>object</code>                                   |
| width      | <code>number</code>                                   |
| height     | <code>number</code>                                   |
| data       | <code>Uint16Array</code> \| <code>Float32Array</code> |
| format     | <code>1023</code> \| <code>1028</code>                |
| colorSpace | <code>&quot;&quot;</code> \| <code>srgb-linear</code> |

<!-- api-end -->

## License

MIT. See [license file](https://github.com/dmnsgn/parse-exr/blob/main/LICENSE.md).
