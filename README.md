# Repolex Knowledge Graph of NousResearch/hermes-desktop-accent-picker

RDF knowledge graph data for [NousResearch/hermes-desktop-accent-picker](https://github.com/NousResearch/hermes-desktop-accent-picker), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/hermes-desktop-accent-picker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 78ef873cddcac876c8a1d12e8a8653befa0646ab
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 78ef873cddcac876c8a1d12e8a8653befa0646ab.nq.gz
│   └── repolex
│       └── 78ef873cddcac876c8a1d12e8a8653befa0646ab
│           └── chunk-001.nq.gz
├── blob
│   ├── 184a4b7fdbbdf5243b91affb827bf1929e0a3a0f.nq.gz
│   ├── 7539c2238e54942e20adb469f5889815077a17e3.nq.gz
│   ├── 75410e73319c72cd3e991a501c5455eb78f38375.nq.gz
│   ├── 7badc780c42849919946b0012d2d231ceff47e2b.nq.gz
│   ├── 82d610632aba1be4bf81107e558643c204816913.nq.gz
│   ├── c2658d7d1b31848c3b71960543cb0368e56cd4c7.nq.gz
│   └── d5943574b95dda4c8cd6b4d2e8f8c43b1b97a14f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 78ef873cddcac876c8a1d12e8a8653befa0646ab.nq.gz
├── filetree
│   └── 78ef873cddcac876c8a1d12e8a8653befa0646ab.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 16 files
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

[NousResearch/hermes-desktop-accent-picker](https://github.com/NousResearch/hermes-desktop-accent-picker)

---
*Parsed on 2026-10-01 by [repolex](https://repolex.ai)*
