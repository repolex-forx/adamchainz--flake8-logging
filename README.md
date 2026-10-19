# Repolex Knowledge Graph of adamchainz/flake8-logging

RDF knowledge graph data for [adamchainz/flake8-logging](https://github.com/adamchainz/flake8-logging), parsed by [repolex](https://repolex.ai).

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
rlex download adamchainz/flake8-logging
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ee5d482b790ce6b3bddca67f58be9dab8e1e2559
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ee5d482b790ce6b3bddca67f58be9dab8e1e2559
│           └── chunk-001.nq.gz
├── blob
│   ├── 205ab9ad9df4ab629d1b7b8d8a72b41f44d8824c.nq.gz
│   ├── 22ddbb118475b52ce8ecba56d9ec45009923da58.nq.gz
│   ├── 2a7f84f54867d02714727f82eef95d3be939d666.nq.gz
│   ├── 30acc83b6797da94e6f047ba88ccfb5b934894ee.nq.gz
│   ├── 3ba13e0cec6cbbfd462e9ebf529dd2093148cd69.nq.gz
│   ├── 40f4ac757715bb1a8c355eda9124141fdda3aeff.nq.gz
│   ├── 438d629c3ce988e3afffa71110b9660853d38549.nq.gz
│   ├── 47eb5f4980a8dc1b20970d00c935978399256eab.nq.gz
│   ├── 663d6b920407c6318f1222445b39e30e44afa9d3.nq.gz
│   ├── 66ea536b4ab7e8552f610c49ab024c14e3b78d92.nq.gz
│   ├── 7f1d007c01048570d774e58f46203d3e92056c39.nq.gz
│   ├── 93acb639926ccf42e9a2f76f02419eeaf0405c3a.nq.gz
│   ├── a559abae6ecb556797114eda5eb004e9613d31e2.nq.gz
│   ├── cea08e8e3f5c1dea9320d164b77717dd0251ae59.nq.gz
│   ├── cf4bca22e6d1dd6e79d5c283f94302e5483a0068.nq.gz
│   ├── d80ff0a66540a6b7e070baddc003099d90e8b847.nq.gz
│   ├── dac3e7440255c70b9415ee41e3810b8c306e2500.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ea55c818091acebfa6ba102d0538182f1ce54f1d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ee5d482b790ce6b3bddca67f58be9dab8e1e2559.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[adamchainz/flake8-logging](https://github.com/adamchainz/flake8-logging)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
