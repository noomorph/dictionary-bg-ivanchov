# dictionary-bg-ivanchov

Bulgarian spelling dictionary according to the orthography introduced by Todor Ivanchov in 1899.

## What is this?

This is a spelling dictionary of the Bulgarian language in the Ivanchov 1899 orthography.
It is based on the extracted [Firefox extension](https://addons.mozilla.org/en-US/firefox/addon/словникъ-български-иванчевски-/)
provided by [Иванчевски Правописъ](http://ivanchevski.grazhdani.eu),
normalized and packaged so that it can be installed and used like other dictionaries.

## When should I use this?

You can use this package when integrating with tools that perform spell checking
(such as [`nodehun`][nodehun], [`nspell`][nspell]) or when making such tools.

## Install

In Node.js (version 14.14+, 16+ or 18+), install with [npm]:

```sh
npm install dictionary-bg-ivanchov
```

## Use

```js
import dictionaryBg from 'dictionary-bg-ivanchov'

dictionaryBg(function (error, bg1899) {
  if (error) throw error
  console.log(bg1899)
  // To do: use `bg1899` somehow
})
```

Yields:

```js
{dic: <Buffer>, aff: <Buffer>}
```

Where `dic` and `aff` are [`Buffer`][buffer]s for `index.dic` and `index.aff`
respectively.

## Examples

See the [monorepo readme][dictionaries] for examples.

## Types

This package is typed with [TypeScript][].

## Contribute

Please [open an issue](https://github.com/noomorph/dictionary-bg-ivanchov/issues/new) on GitHub.

## License

Dictionary and affix file: [GPL-3.0](https://github.com/noomorph/dictionary-bg-ivanchov/blob/main/LICENSE).
Rest: [MIT][] © [Titus Wormer][home].

[hunspell]: https://hunspell.github.io

[nodehun]: https://github.com/nathanjsweet/nodehun

[nspell]: https://github.com/wooorm/nspell

[macos]: https://github.com/wooorm/dictionaries#example-use-with-macos

[npm]: https://docs.npmjs.com/cli/install

[dictionaries]: https://github.com/wooorm/dictionaries

[mit]: https://github.com/wooorm/dictionaries/blob/main/license

[buffer]: https://nodejs.org/api/buffer.html#buffer_buffer

[home]: https://wooorm.com

[typescript]: https://www.typescriptlang.org
