# Repolex Knowledge Graph of realpython/pytest-mypy

RDF knowledge graph data for [realpython/pytest-mypy](https://github.com/realpython/pytest-mypy), parsed by [repolex](https://repolex.ai).

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
rlex download realpython/pytest-mypy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b578993c4cbb4bbf3f16aceef123b67825fe5aff
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b578993c4cbb4bbf3f16aceef123b67825fe5aff
│           └── chunk-001.nq.gz
├── blob
│   ├── 0db2324608427ed6a9287751cb69f777294367e5.nq.gz
│   ├── 2306bcc9daa419097086b6c3fff51f7302f650af.nq.gz
│   ├── 26b71fba5d7f5683805adbb454b0a94fdd1f160d.nq.gz
│   ├── 4a19aa0f59eed843f65213fc364117ab535fbb09.nq.gz
│   ├── 803bbe64a70b7e8728c7f6284810e127013d8e06.nq.gz
│   ├── 962681b209360c7ec8905cdd82b1c21f37e20dae.nq.gz
│   ├── a4455fbc19c158a928d1db96d2f53e9f6afd2486.nq.gz
│   ├── a71c33667d50a8fe17c143ddfdd2ebbd24710018.nq.gz
│   ├── b12ace61523f6198a23aa9ba695383ea859084bf.nq.gz
│   ├── ba1bf816d43b0887a2e5168aefa79042513c8b6e.nq.gz
│   ├── c0c219be58d95f4851ae22d8869fbcc47a5d0b29.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ef37f37715a0c9e0d97e10dacd48722acfc2ebc6.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b578993c4cbb4bbf3f16aceef123b67825fe5aff.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[realpython/pytest-mypy](https://github.com/realpython/pytest-mypy)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
