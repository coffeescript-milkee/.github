<div align="center">

<a href="https://milkee.org"><img src="https://raw.githubusercontent.com/coffeescript-milkee/milkee/main/img/Milkee-logo.png" width="480" alt="Milkee logo"></a>

**A modern build tool for CoffeeScript. Simple, fast, and creamy smooth.**

[Official site](https://milkee.org) · [npm](https://www.npmjs.com/package/milkee) · [Repository](https://github.com/coffeescript-milkee/milkee)

</div>

Milkee builds CoffeeScript projects from a single `coffee.config.cjs`: point it at an entry and an output, set the `coffee` compiler options you need (source maps, `join`, Babel transpile, watch mode), and extend the build with plugins that run after each successful compile.

```bash
npm i -D milkee coffeescript   # add @babel/core too if you use options.transpile
npx milkee -s                  # generate coffee.config.cjs
npx milkee                     # build
```

## Packages

| Package | What it does |
| --- | --- |
| [`milkee`](https://github.com/coffeescript-milkee/milkee) [![npm](https://img.shields.io/npm/v/milkee)](https://www.npmjs.com/package/milkee) | The build tool and its `milkee` CLI |
| [`@milkee/d`](https://github.com/coffeescript-milkee/declare) [![npm](https://img.shields.io/npm/v/@milkee/d)](https://www.npmjs.com/package/@milkee/d) | Type definitions for `coffee.config.cjs` (`/** @type {import('@milkee/d').Config} */`) |

### Plugins

| Plugin | What it does |
| --- | --- |
| [`milkee-plugin-ext`](https://github.com/coffeescript-milkee/milkee-plugin-ext) [![npm](https://img.shields.io/npm/v/milkee-plugin-ext)](https://www.npmjs.com/package/milkee-plugin-ext) | Rewrites `.coffee` / `.litcoffee` extensions to `.js` in `import` and `require` |
| [`milkee-plugin-copy`](https://github.com/coffeescript-milkee/milkee-plugin-copy) [![npm](https://img.shields.io/npm/v/milkee-plugin-copy)](https://www.npmjs.com/package/milkee-plugin-copy) | Fine-grained control over files copied to the output (glob patterns, removing matched files after compile) |
| [`milkee-plugin-minify`](https://github.com/coffeescript-milkee/milkee-plugin-minify) [![npm](https://img.shields.io/npm/v/milkee-plugin-minify)](https://www.npmjs.com/package/milkee-plugin-minify) | Minifies the compiled JavaScript |
| [`milkee-plugin-obfuscator`](https://github.com/coffeescript-milkee/milkee-plugin-obfuscator) [![npm](https://img.shields.io/npm/v/milkee-plugin-obfuscator)](https://www.npmjs.com/package/milkee-plugin-obfuscator) | Obfuscates the compiled JavaScript |
| [`milkee-plugin-shebang`](https://github.com/coffeescript-milkee/milkee-plugin-shebang) [![npm](https://img.shields.io/npm/v/milkee-plugin-shebang)](https://www.npmjs.com/package/milkee-plugin-shebang) | Adds `#!/usr/bin/env node` to compiled files |
| [`milkee-plugin-prettier`](https://github.com/coffeescript-milkee/milkee-plugin-prettier) [![npm](https://img.shields.io/npm/v/milkee-plugin-prettier)](https://www.npmjs.com/package/milkee-plugin-prettier) | Formats the `.coffee` sources in the entry directory with Prettier, without version conflicts |
| [`milkee-plugin-lsc`](https://github.com/coffeescript-milkee/milkee-plugin-lsc) [![npm](https://img.shields.io/npm/v/milkee-plugin-lsc)](https://www.npmjs.com/package/milkee-plugin-lsc) | Handles LiveScript in Milkee |

A plugin is a plain function that runs after each successful compile. See the [plugin guide](https://github.com/coffeescript-milkee/milkee/blob/main/docs/PLUGIN.md) ([日本語](https://github.com/coffeescript-milkee/milkee/blob/main/docs/PLUGIN-ja.md)) to write your own.

## Website

The official site [milkee.org](https://milkee.org) is built from [`docs`](https://github.com/coffeescript-milkee/docs).

## Author

otoneko. https://github.com/otnc

All packages are MIT licensed.
