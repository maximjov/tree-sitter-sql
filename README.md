# tree-sitter-sql

[![npm package version](https://img.shields.io/npm/v/%40derekstride/tree-sitter-sql?logo=npm&color=brightgreen)](https://www.npmjs.com/package/@maximjov/tree-sitter-sql)

A general/permissive SQL grammar for [tree-sitter](https://github.com/tree-sitter/tree-sitter) adapted by @maximjov for use in [pg_lens](https://github.com/mmoncure/pg_lens)

## Installation

I'm open to feedback & encourage you to [open an issue](https://github.com/maximjov/tree-sitter-sql/issues/new) to discuss any features or problems with changes.

For any issues related to non-forked related problems, you can open an issue in the [original project](https://github.com/DerekStride/tree-sitter-sql/issues/new) by @DerekStride

### Step 1: Download the parser files

**Using `git`**
```bash
git clone https://github.com/DerekStride/tree-sitter-sql.git
cd tree-sitter-sql
git checkout gh-pages
```

**Using `curl`**
```bash
curl -LO https://github.com/DerekStride/tree-sitter-sql/archive/refs/heads/gh-pages.tar.gz
tar -xzf gh-pages.tar.gz
cd tree-sitter-sql-gh-pages
```

### Step 2: Build yourself

### Using [npm](https://www.npmjs.com/package/@maximjov/tree-sitter-sql)

FIRST
```bash
npm install
```

```bash
rm -rf build src/parser.c src/parser.cc src/scanner.o
tree-sitter generate -b --libdir ./build
npm rebuild
```
OR
```bash
npm run build
```

#### link or local install

```bash
npm i path_to_repo
```
```bash
npm link # in "@maximjov/tree-sitter-sql" root
...
npm link @maximjov/tree-sitter-sql # in other root
```

### Step 2: Compile the Parser (if not building locally)

### Using [npm](https://www.npmjs.com/package/@maximjov/tree-sitter-sql)
#### only supporting NPM at the moment, feel free to try methods mentioned in the [original project](https://github.com/DerekStride/tree-sitter-sql/issues/new)

```bash
npm i @maximjov/tree-sitter-sql
```

## Development

See [CONTRIBUTING.md](CONTRIBUTING.md) for documentation on how to set up the project for development.

## Features

For a complete list of features see the the [tests](test/corpus)

## References

* [Wikipedia#SQL_syntax](https://en.wikipedia.org/wiki/SQL_syntax) - I consulted wikipedia for naming conventions,
  though I may not have been strict early on in the prototyping.
* [Phoenix Language Reference](https://forcedotcom.github.io/phoenix/index.html) - A reference diagram.
* [SQLite's railroad diagram for expr](https://www.sqlite.org/lang_expr.html) - Another reference diagram.
* [Postgresql syntax documentation](https://www.postgresql.org/docs/current/sql-commands.html)
* [Mariadb syntax documentation](https://mariadb.com/kb/en/sql-statements-structure/)

### Other projects

* https://github.com/m-novikov/tree-sitter-sql
* https://github.com/tjdevries/tree-sitter-sql
* https://github.com/dhcmrlchtdj/tree-sitter-sqlite
