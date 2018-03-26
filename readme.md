# lunchtype.css

Lunchtype fonts as a node packaged module.

[![latest version][npm-img]][npm-url] [![build status][travis-img]][travis-url] [![stability][stability-img]][stability-url] [![downloads][downloads-img]][npm-url]

[npm-img]: https://img.shields.io/npm/v/lunchtype.css.svg?style=flat-square
[npm-url]: https://www.npmjs.com/package/lunchtype.css
[travis-img]: https://img.shields.io/travis/bcomnes/lunchtype.css.svg?style=flat-square
[travis-url]: https://travis-ci.org/bcomnes/lunchtype.css
[stability-img]: https://img.shields.io/badge/stability-stable-brightgreen.svg?style=flat-square
[stability-url]: https://iojs.org/api/documentation.html#documentation_stability_index
[downloads-img]: https://img.shields.io/npm/dm/lunchtype.css.svg?style=flat-square

## Install

```sh
$ npm install lunchtype.css
```

The css is exported from the package.json `main` field and can be imported using a css bundler or copied out of `node_modules` as part of a larger build process.

## Usage

```css
@import "lunchtype.css"; /* or @import "lunchtype.css/LunchType22/Web/stylesheets.css"; */
.lunchtype-regular { font-family: "lunchtype22regular", sans-serif; }
.lunchtype-medium { font-family: "lunchtype22medium", sans-serif; }
.lunchtype-light { font-family: "lunchtype22light", sans-serif; }

@import "lunchtype.css/LunchType23/Web/stylesheets.css";
.lunchtype-italic { font-family: "lunchtype23italic", sans-serif; }
.lunchtype-medium_italic { font-family: "lunchtype23medium_italic", sans-serif; }
.lunchtype-light_italic { font-family: "lunchtype23light_italic", sans-serif; }

@import "lunchtype.css/LunchType24/Web/stylesheets.css";
.lunchtype-expanded_regular { font-family: "lunchtype24expanded_regular", sans-serif; }
.lunchtype-expanded_medium { font-family: "lunchtype24expanded_medium", sans-serif; }
.lunchtype-expanded_light { font-family: "lunchtype24expanded_light", sans-serif; }

@import "lunchtype.css/LunchType25/Web/stylesheets.css";
.lunchtype-condensed_light { font-family: "lunchtype25condensed_light", sans-serif; }
.lunchtype-condensed_medium { font-family: "lunchtype25condensed_medium", sans-serif; }
.lunchtype-condensed_regular { font-family: "lunchtype25condensed_regular", sans-serif; }
```

### PostCSS

You can use PostCSS to inline and import this css module using the following `postcss.config.js`:

```js
module.exports = (ctx) => ({
  plugins: {
    'postcss-import': { root: ctx.file.dirname }, // Inline module css
    'postcss-url': { // Copy assets from node_modules
      url: 'copy',
      useHash: true,
      assetsPath: 'assets'
    }
  }
})
```

```
$ postcss styles.css -o dist/bundle.css
```
- [postcss/postcss](https://ghub.io/postcss)
- [jantimon/postcss-inline](https://github.com/jantimon/postcss-inline)
- [postcss/postcss-url](https://github.com/postcss/postcss-url)

## Credits

- [lunchtype.com](http://lunchtype.com)

## See also

- [style.css](https://github.com/ungoldman/style.css)
- [top-bar.css](https://github.com/ungoldman/top-bar.css)
- [fraktur.css](https://github.com/bcomnes/fraktur.css)
- [chigaco.css](https://github.com/bcomnes/chicago.css)
- [big-cursors.css](https://github.com/bcomnes/big-cursors.css)