# Repolex Knowledge Graph of aio-libs/sphinxcontrib-asyncio

RDF knowledge graph data for [aio-libs/sphinxcontrib-asyncio](https://github.com/aio-libs/sphinxcontrib-asyncio), parsed by [repolex](https://repolex.ai).

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
rlex download aio-libs/sphinxcontrib-asyncio
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 0cef4f21ae6aab6b8285ad171f8cdf47429d37a0
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 0cef4f21ae6aab6b8285ad171f8cdf47429d37a0
│           └── chunk-001.nq.gz
├── blob
│   ├── 0b2f7b0655f41276d418ca8302dbaec8b7e7e829.nq.gz
│   ├── 15d3ff2f3ed2456710a70cc79426410d5be012da.nq.gz
│   ├── 1dbc687de014ee027b4e6c0d7f2a37ee7636137e.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 6ce0aec2dc936d5fc1075a1373ff52b1a6d7f68f.nq.gz
│   ├── 6ff1938e7e38c0ce8bfc59a080fa77240704ef31.nq.gz
│   ├── 7412fd91484e50c2e49c97b1550902178bed4a45.nq.gz
│   ├── b5077be47c6a03e1044098794301b8536d863c9b.nq.gz
│   ├── c7f7d635383c997a29f04438cd73fbbffd7c9133.nq.gz
│   ├── cfbec44c0114261a6b99506e0ba789f898d4c9fc.nq.gz
│   ├── dcde6e8d64672dc03e279135fcf90c1f8d8a835c.nq.gz
│   ├── de40ea7ca058e07a399acf61529d418c07eeee61.nq.gz
│   ├── e4884423f1f3c28f1f01d03c9e676127547b57c0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f6b693cc864a7eebb8c604c54c5a525ab8518f63.nq.gz
│   ├── f9b706d6c11d9195ae3c997e613389b219a20e5f.nq.gz
│   └── fa0e69057437a6b4ed14896dd8c18043162c94d6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 0cef4f21ae6aab6b8285ad171f8cdf47429d37a0.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[aio-libs/sphinxcontrib-asyncio](https://github.com/aio-libs/sphinxcontrib-asyncio)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
