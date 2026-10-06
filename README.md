# tree-sitter-burn

A [tree-sitter](https://tree-sitter.github.io) grammar for [Burn](https://github.com/burnlang/burn), with highlight
queries. The [Zed extension](https://github.com/burnlang/zed-burn) uses it, and Neovim (through nvim-treesitter),
Helix and other tree-sitter editors can too.

It covers the whole language: `def` definitions with modifiers and annotations, functions in both parameter styles,
generics, `match`, string templates, closures, `is`/`as` casts and the null-safe operators.

## Development

```sh
npm install -g tree-sitter-cli@0.25.10
tree-sitter generate --abi 14
tree-sitter test
tree-sitter parse path/to/file.bn
```

Commit the regenerated `src/` with every change to `grammar.js`; CI checks that it is up to date, runs the corpus
tests in `test/corpus` and parses every `.bn` file of the Burn repository.

## License

GPL-3.0-only
