# @taktikorg/dicta-ex <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Validate an object in the "exports" field.

## Example

```js
const assert = require('assert');
const validateExportsObject = require('@taktikorg/dicta-ex');
const pkg = require('./package.json');

const results = validateExportsObject(pkg.exports);

assert.deepEqual(
    results,
    {
        __proto__: null,
        normalized: {
            __proto__: null,
            '.': './index.js',
            './package.json': './package.json'
        },
        problems: [],
        status: 'files'
    }
);
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Security

Please email [@ljharb](https://github.com/ljharb) or see https://tidelift.com/security if you have a potential security vulnerability to report.

[package-url]: https://npmjs.org/package/@taktikorg/dicta-ex
[npm-version-svg]: https://versionbadg.es/ljharb/@taktikorg/dicta-ex.svg
[deps-svg]: https://david-dm.org/ljharb/@taktikorg/dicta-ex.svg
[deps-url]: https://david-dm.org/ljharb/@taktikorg/dicta-ex
[dev-deps-svg]: https://david-dm.org/ljharb/@taktikorg/dicta-ex/dev-status.svg
[dev-deps-url]: https://david-dm.org/ljharb/@taktikorg/dicta-ex#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@taktikorg/dicta-ex.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@taktikorg/dicta-ex.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@taktikorg/dicta-ex.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@taktikorg/dicta-ex
[codecov-image]: https://codecov.io/gh/ljharb/@taktikorg/dicta-ex/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/ljharb/@taktikorg/dicta-ex/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/ljharb/@taktikorg/dicta-ex
[actions-url]: https://github.com/taktikorg/dicta-ex/actions
