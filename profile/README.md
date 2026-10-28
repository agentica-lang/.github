# Agentica

Agentica is Ruby with static types: a small language with Ruby-like syntax. Every program is checked before it runs, and values never change in place. It stays small on purpose, so people and AI agents can write, read and fix programs with few surprises. Every error has a stable code, a source position and often a hint with the fix.

A front end written in Agentica compiles each program to bytecode, and a C VM runs it. Both ship as one binary, `agentica`.

```ruby
## Returns the price with the tax added.
def with_tax(cents: Int) -> Int
  return cents + cents * 21 / 100
end

def main() -> Void
  total = [250, 1_000, 99].map(&with_tax).sum
  puts("total: #{total} cents")
end
```

## Repositories

| Repository | What it is |
|---|---|
| [agentica](https://github.com/agentica-lang/agentica) | The language: compiler, VM, standard library and docs |
| [agentica-db](https://github.com/agentica-lang/agentica-db) | Database package: one API for PostgreSQL, SQLite and MySQL, through the FFI |
| [agc-lsp](https://github.com/agentica-lang/agc-lsp) | Language server (LSP), written in Agentica |
| [tree-sitter-agentica](https://github.com/agentica-lang/tree-sitter-agentica) | Tree-sitter grammar |
| [agc-tmlanguage](https://github.com/agentica-lang/agc-tmlanguage) | TextMate grammar for syntax highlighting |

## Links

- [Documentation](https://agentica-lang.github.io/agentica/)
- [Install guide](https://agentica-lang.github.io/agentica/getting-started/)
- [Releases](https://github.com/agentica-lang/agentica/releases)
