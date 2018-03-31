# shopify-cp

> utility module for copying various aspects of shopify sites from a source site to duplicate (sink) site

this module is a collection of other `shopify-*-cp` modules.
each method has the same api of `cp[method](source, sink)` 

the return value of each method is a stream response from shopify

## Usage

```js
var cp = require('shopify-cp')

// use every method (copy everything we can right now)
Object.keys(cp).forEach(function (api) {
  cp[api](source, sink).pipe(process.stdout)
})

// or use individual methods
cp.pages(source, sink).pipe(process.stdout)
cp.products(source, sink).pipe(process.stdout)
```

## API

```js
var cp = require('shopify-cp')
```

```js
cp.pages(source, sink)
```

```js
cp.products(source, sink)
```

pull request welcome to add more api methods! :)

## Install

With [npm](https://npmjs.org/) installed, run

```
$ npm install shopify-cp
```

## See Also

- [`jekrb/shopify-pages-cp`](https://github.com/jekrb/shopify-pages-cp)
- [`jekrb/shopify-products-cp`](https://github.com/jekrb/shopify-products-cp)

## License

MIT

