# prettier-config

A shared [Prettier](https://prettier.io/) config: Prettier's defaults, without semicolons, and with trailing commas only where ES5 allows them.

## Install

```sh
npm install --save-dev @ycookiey/prettier-config prettier
```

Requires Prettier 3.

## Usage

Add the `prettier` key to your `package.json`:

```json
{
  "prettier": "@ycookiey/prettier-config"
}
```

Or write the package name in `.prettierrc`:

```json
"@ycookiey/prettier-config"
```

To change some options, use a JavaScript config. The config is a JSON file, so import it with the `type: "json"` attribute:

```js
// prettier.config.mjs
import config from "@ycookiey/prettier-config" with { type: "json" };

export default {
  ...config,
  printWidth: 100,
};
```

## Options

Two options differ from Prettier's defaults:

| option | this config | Prettier's default |
|---|---|---|
| `semi` | `false` | `true` |
| `trailingComma` | `"es5"` | `"all"` |

The config also sets `printWidth`, `tabWidth`, `useTabs`, `singleQuote`, `quoteProps`, `jsxSingleQuote`, `bracketSpacing`, `arrowParens` and `endOfLine` to Prettier's default values, so a later Prettier release that changes one of these defaults does not change your formatting.

## License

[MIT](LICENSE)
