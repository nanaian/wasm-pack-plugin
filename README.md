# @wasm-tool/rust-loader

> Webpack loader for Rust

## Installation

```sh
yarn add --dev @wasm-tool/rust-loader
```

### `wasm-pack`

We expect `wasm-pack` to be in your `$PATH`. See [installation here](https://github.com/rustwasm/wasm-pack/blob/master/docs/setup.md#installing-wasm-pack).

## Usage

Add the loader in your `webpack.config.js`:

```js
module.exports = {
  // ...

  module: {
    rules: [
      {
        test: /\.rs$/,
        loader: "@wasm-tool/rust-loader"
      }
    ]
  },

  // ...
};
```

and then import your `lib.rs` file:

```js
import("./lib.rs").then(module => {
  module.run();
});
```
