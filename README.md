# Repolex Knowledge Graph of pallets-eco/.github

RDF knowledge graph data for [pallets-eco/.github](https://github.com/pallets-eco/.github), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/.github
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── aa505cc7eacd230c344519e739120bef27b1dbce
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── aa505cc7eacd230c344519e739120bef27b1dbce
│           └── chunk-001.nq.gz
├── blob
│   ├── 01946040621943c6309a9584fe13ab33b7125537.nq.gz
│   ├── 17cd6bed3c0392591e65e57162f8203094d98097.nq.gz
│   ├── 31954510b7067fc761286583173a0bdaf03f066a.nq.gz
│   ├── 8a2eda34304fa14e1cc3d1ae4ee94d1dfc65df49.nq.gz
│   └── a51ce41a726db60f4ef8b0252c79dbf542e09485.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── aa505cc7eacd230c344519e739120bef27b1dbce.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 12 files
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

[pallets-eco/.github](https://github.com/pallets-eco/.github)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
