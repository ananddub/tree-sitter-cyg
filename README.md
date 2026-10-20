# tree-sitter-cyg

Tree-sitter grammar for the CYG deterministic simulation schema language.

The grammar covers the full surface language: `namespace`, `asset`, `struct`,
`component`, `enum`, `flags`, `union`, `input`, `global`, `event`,
`synced_event`, and `signal`, including every builtin, `QString<N>`,
`asset_ref<T>`, and the fixed `array`/`list`/`dictionary` containers.

## Queries

| File | Consumer |
| --- | --- |
| `queries/highlights.scm` | Syntax highlighting |
| `queries/outline.scm` | Code outline / breadcrumbs |
| `queries/indents.scm` | Auto-indentation |
| `queries/brackets.scm` | Rainbow and matching brackets |

## Development

```bash
npm install
npx tree-sitter generate
npx tree-sitter parse path/to/file.cyg
npx tree-sitter query queries/highlights.scm path/to/file.cyg
```

The generated parser in `src/` is committed so editors and the Zed extension
can build the grammar without running the Tree-sitter CLI.

## Used by

- [cyg-zed](https://github.com/ananddub/cyg-zed) — CYG language support for Zed.

## License

MIT
