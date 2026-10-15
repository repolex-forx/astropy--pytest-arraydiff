# Repolex Knowledge Graph of astropy/pytest-arraydiff

RDF knowledge graph data for [astropy/pytest-arraydiff](https://github.com/astropy/pytest-arraydiff), parsed by [repolex](https://repolex.ai).

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
rlex download astropy/pytest-arraydiff
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 12e95c06cd1ef64e34200becc5cd5b81eefb5bdf
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 12e95c06cd1ef64e34200becc5cd5b81eefb5bdf
│           └── chunk-001.nq.gz
├── blob
│   ├── 1e60a17eac0a832adea27ed7f0e3198639a9bc13.nq.gz
│   ├── 2e452d9818fac75f748a22a4146e8e2f3cb8de85.nq.gz
│   ├── 31fbcad26fadcfb2c5d009517dc99796f0397803.nq.gz
│   ├── 36efcb109dd5aeae31b01804865641963c8a25ee.nq.gz
│   ├── 37f21a54b050478f9dd8a0c88dfabe27ab907dfd.nq.gz
│   ├── 3d752e0c6f6c8ecde3540048e4c8ca25aae8db95.nq.gz
│   ├── 49bbd47f40d5758236b8a244ac5c5ec6f41559d1.nq.gz
│   ├── 6b5ccefab1a9297df4c6d1a30881dd90726485c5.nq.gz
│   ├── 6d955cdefc652bb831a22866f557437f8dd5dc48.nq.gz
│   ├── 72e56d177c073b534b78ffc302721b5c1f4c645f.nq.gz
│   ├── 7e17ccd397263814b1dfadc20c7994f0d913448f.nq.gz
│   ├── 8b8ebcc690eccac11585517c67b0af23b63cf444.nq.gz
│   ├── 93b22c3b0cef07613902b8acfa6470c2e3a3199e.nq.gz
│   ├── 9fab1aecec0b5b4ebc8f9fbcacbf001d054bd68d.nq.gz
│   ├── b507b35474ebf2eb9aeb41a0a0b918e0c6c1464b.nq.gz
│   ├── c6481d5f740462ec9fd3edcb32aa56806e316c77.nq.gz
│   ├── e77c5535ab04549ef332c4106b3a0912de396dd7.nq.gz
│   ├── ec8a646cbee9bc34ebb8bfb9e070376224117cfd.nq.gz
│   ├── f345de56381c996f9f65e162b3dc3ad3e52db85b.nq.gz
│   └── fca8de1469e9e22bd12062258da1126d0283ebdd.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 12e95c06cd1ef64e34200becc5cd5b81eefb5bdf.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[astropy/pytest-arraydiff](https://github.com/astropy/pytest-arraydiff)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
