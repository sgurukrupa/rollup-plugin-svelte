# rollup-plugin-svelte

Compile Svelte components.


## Installation

```bash
npm install --save-dev rollup-plugin-svelte
```


## Usage

```js
// rollup.config.js
import svelte from 'rollup-plugin-svelte';

export default {
  entry: 'src/main.js',
  dest: 'bundle.js',
  format: 'iife',
  plugins: [
    svelte({
      // By default, all .html and .svelte files are compiled
      extensions: [ '.my-custom-extension' ],

      // You can restrict which files are compiled
      // using `include` and `exclude`
      include: 'src/components/**/*.html',

      // By default, the client-side compiler is used. You
      // can also use the server-side rendering compiler
      generate: 'ssr',

      // If you're doing server-side rendering, you may want
      // to prevent the client-side compiler from duplicating CSS
      css: false
    })
  ]
}
```

## License

MIT
