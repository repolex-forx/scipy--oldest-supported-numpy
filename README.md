# Repolex Knowledge Graph of scipy/oldest-supported-numpy

RDF knowledge graph data for [scipy/oldest-supported-numpy](https://github.com/scipy/oldest-supported-numpy), parsed by [repolex](https://repolex.ai).

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
rlex download scipy/oldest-supported-numpy
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 687ffc2f57e29ec7c74a28c58c247d16d0f6bee1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 687ffc2f57e29ec7c74a28c58c247d16d0f6bee1
│           └── chunk-001.nq.gz
├── blob
│   ├── 15f6eb1f17855ac7ed52bcfdc55e38d9d35429b3.nq.gz
│   ├── 2b6d0846cd86a39cc4ad71e27a79f4330a5deaf0.nq.gz
│   ├── 2b90bb6dfa738f1caeab246a38590a432df715c5.nq.gz
│   ├── 2fb97ee7c154740cde01b573b1a2185e78b25bd9.nq.gz
│   ├── 3b4a3a3343d472499793b66eb95f993ac5b55cea.nq.gz
│   ├── 3f7bc1ab73d3ffe6b8fc538a86238ce3d0dfd4e5.nq.gz
│   ├── 633538f1c9a98ebeb53925f7b8c8676dc2442b84.nq.gz
│   ├── 7ffad827172b6fe54639d95d0458ba23f97ecbf5.nq.gz
│   ├── b6ca80d6c56d6897f291a742bdc08b7ac608b6e7.nq.gz
│   ├── c18dd8d83ceed1806b50b0aaa46beb7e335fff13.nq.gz
│   ├── d8f1eb1bf6bb2e3710593964caa3d6643e009c15.nq.gz
│   └── ea0c10623ebf589f7ae5e6ddbd5663b75f8d8dab.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 687ffc2f57e29ec7c74a28c58c247d16d0f6bee1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[scipy/oldest-supported-numpy](https://github.com/scipy/oldest-supported-numpy)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
