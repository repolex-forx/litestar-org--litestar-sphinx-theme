# Repolex Knowledge Graph of litestar-org/litestar-sphinx-theme

RDF knowledge graph data for [litestar-org/litestar-sphinx-theme](https://github.com/litestar-org/litestar-sphinx-theme), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download litestar-org/litestar-sphinx-theme
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cb7cc4bddb876e54f71b19cebb8f3a590d6b51fd
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cb7cc4bddb876e54f71b19cebb8f3a590d6b51fd
│           └── chunk-001.nq.gz
├── blob
│   ├── 021384311c320f1a77baed77ab02a45768b4b3ab.nq.gz
│   ├── 0ae848eb4f1271cd5a2c4e5837cbf694df646469.nq.gz
│   ├── 123014908bebbfb7ecfa1d15daaceb272fabe05b.nq.gz
│   ├── 16d02b09430be2a6ff09a0df34dbb32eed3446fb.nq.gz
│   ├── 1aa85454ebb3c1cd2960a0ad661f966af567adcd.nq.gz
│   ├── 256844a9dd6a2ca1279879f4ed734a6a0c83d20f.nq.gz
│   ├── 2f69e99ebd58ffe5d37d162f92e425bb12fb3b51.nq.gz
│   ├── 38dfc73eba432e47e0f4e2f1cd0dbc0bc8f84eee.nq.gz
│   ├── 3cde5b36fdf1719d6b0fe428c8ce0fec03eda57c.nq.gz
│   ├── 4f7bc4caeb34a7740a8f64fa59a493e57223c47d.nq.gz
│   ├── 51ac66959dc247dbd2d01c13e34e6fcda2911e46.nq.gz
│   ├── 6c55f9504f1f3d62283415a607a7f4afe3a0771b.nq.gz
│   ├── 7a207758a9905d08f1a9f7cf00ad85f21a734694.nq.gz
│   ├── 815dc50876527e3864d8c0c02e22835e3aff045f.nq.gz
│   ├── 84a088924af7b934a9da9e558d8af0770b5be55f.nq.gz
│   ├── 8641707298215c075814eed18160d04c27e835f3.nq.gz
│   ├── a7b775c7eb952466e93ff4bd05d41b4a1f829ff5.nq.gz
│   ├── abd1a65a0e02437c1eec0d9d41f3dc59b51bc215.nq.gz
│   ├── bcfed807ca6fb7e588b09b49f33e7586bcb5a2e9.nq.gz
│   ├── c548112bb9d2a0b0808a330abcb450ba6a780907.nq.gz
│   ├── e83862fe0748d1a5eecbe2068ff261f1552929b9.nq.gz
│   ├── ecc6e43cba90dd52daaea0e7bdc407f5301acf7e.nq.gz
│   ├── f23e8ed555f0c38848658928877e230dbb5a0a95.nq.gz
│   ├── f724ed0d815b8c2569303ccd2252c38c99bb85b2.nq.gz
│   └── fb4cf7c8a8b81bf37aaaa7dca7abd3c06b5d6a8a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cb7cc4bddb876e54f71b19cebb8f3a590d6b51fd.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[litestar-org/litestar-sphinx-theme](https://github.com/litestar-org/litestar-sphinx-theme)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
