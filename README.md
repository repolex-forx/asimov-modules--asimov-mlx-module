# Repolex Knowledge Graph of asimov-modules/asimov-mlx-module

RDF knowledge graph data for [asimov-modules/asimov-mlx-module](https://github.com/asimov-modules/asimov-mlx-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-mlx-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── fafb79875a38b57b322acb3d74e818c2d8cda564
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── fafb79875a38b57b322acb3d74e818c2d8cda564.nq.gz
│   └── repolex
│       └── fafb79875a38b57b322acb3d74e818c2d8cda564
│           └── chunk-001.nq.gz
├── blob
│   ├── 10b359dd05935c73efb064470f9ecda90f6d28aa.nq.gz
│   ├── 496819498f0503ff7705b01321892b22930b1cb4.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6dc86a6570481199b1afce40a6260c79945ab3a4.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 7748ae802561167648da53b25d0e6ec4db1a4025.nq.gz
│   ├── 8b9c783fd3a2a66ddcdc0af380907366c971a593.nq.gz
│   ├── 9fe50de16e59d550235aa6d7d15ee12ddf054414.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── ab9af129b48a7f81521041ac3a687a5a23ec49e3.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── bcab45af15a0f1b0166daf8cbf18b17cd8649277.nq.gz
│   ├── cb76e98e611506b3bb9cca2da105ffdddd69e677.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── d53e657fb34f6560e7b9bcf999a0eb3566f25848.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── fafb79875a38b57b322acb3d74e818c2d8cda564.nq.gz
├── filetree
│   └── fafb79875a38b57b322acb3d74e818c2d8cda564.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[asimov-modules/asimov-mlx-module](https://github.com/asimov-modules/asimov-mlx-module)

---
*Parsed on 2026-09-27 by [repolex](https://repolex.ai)*
