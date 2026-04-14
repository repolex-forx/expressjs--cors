# Repolex Knowledge Graph of expressjs/cors

RDF knowledge graph data for [expressjs/cors](https://github.com/expressjs/cors), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download expressjs/cors
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── f00a8c1f0af727ffe5ed35f3b2d0b1a7eb4b65bb
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── f00a8c1f0af727ffe5ed35f3b2d0b1a7eb4b65bb.nq.gz
│   └── repolex
│       └── f00a8c1f0af727ffe5ed35f3b2d0b1a7eb4b65bb
│           └── chunk-001.nq.gz
├── blob
│   ├── 32746dc3a0a2fdeaff41a14d73200c23ca5ef3c1.nq.gz
│   ├── 34ddb41b73d74ac29638b5c2168b7e2b397d2302.nq.gz
│   ├── 3d206e5b6fe5177f539a239e9a3e6d7dfde27808.nq.gz
│   ├── 4ae1a3a4bd66c6abc1af353f421930d918b338d0.nq.gz
│   ├── 85830e2a6eaa2e1b16f926be3e85147d675e7259.nq.gz
│   ├── 89676d93967278ed0bb353e8eace66bfe52dd579.nq.gz
│   ├── 9808c3b2b6602da61eb4afcb4caf33368e3e2bd4.nq.gz
│   ├── ad899cae9539e4cfdf5839528e4a78441d5b847f.nq.gz
│   ├── b9b29f2c5aa306b879568d81abc63baaaa15e38c.nq.gz
│   ├── bd8c6a8b3609d21da66970e84e36bf7adffcec70.nq.gz
│   ├── bdff87f4d13d377a32c9ce2c5d3afde0cb135691.nq.gz
│   ├── e89c288ff0729a1cb508601ca8471cc9fdf567bf.nq.gz
│   ├── e90bac839267110ee7d3b9e1bbeb70ec1834856e.nq.gz
│   ├── eb938f3b7a113949694d5ace9c96b276e4c62359.nq.gz
│   ├── f15b98e249d653f23d7e121037bde0eae1817582.nq.gz
│   ├── fb6c3102d4873f71f182a336dfaa91e852a0e01f.nq.gz
│   └── fd10c843f2bab584e53933b7d1fc445b9aef9bfc.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── f00a8c1f0af727ffe5ed35f3b2d0b1a7eb4b65bb.nq.gz
├── filetree
│   └── f00a8c1f0af727ffe5ed35f3b2d0b1a7eb4b65bb.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 27 files
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

## Source repository

[expressjs/cors](https://github.com/expressjs/cors)

---
*Parsed on 2026-04-14 by [repolex](https://repolex.ai)*
