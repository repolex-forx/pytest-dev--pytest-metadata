# Repolex Knowledge Graph of pytest-dev/pytest-metadata

RDF knowledge graph data for [pytest-dev/pytest-metadata](https://github.com/pytest-dev/pytest-metadata), parsed by [repolex](https://repolex.ai).

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
rlex download pytest-dev/pytest-metadata
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 16b39d2b8ec7500d566ff8b45576ea866d2c719c
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 16b39d2b8ec7500d566ff8b45576ea866d2c719c
│           └── chunk-001.nq.gz
├── blob
│   ├── 019ea016ab4a6fc3a6b5b7037383e8c45cd100d1.nq.gz
│   ├── 02f011e1da07b9c29cb606ae5fb10c3ae05d9d74.nq.gz
│   ├── 032f74a6ea09c440f179177d445eaf08e6a8f2f1.nq.gz
│   ├── 23820f929a7d9d3011cfcfa61c30afa761762634.nq.gz
│   ├── 2c88d995fa70efb29b9f3f5adcdef37e669a8bc3.nq.gz
│   ├── 2f479e96ef514432238681f5fd946bfb4de069d4.nq.gz
│   ├── 350d42e7767734143e35993e6993630b2111632a.nq.gz
│   ├── 410cb51a4fe21d6326246cebad4a39f8d70a135c.nq.gz
│   ├── 41dc2327f1698b99dd397a84f47b9596d0a516b5.nq.gz
│   ├── 4787755d35ce3ca3a50367d5c63481fb51f8be67.nq.gz
│   ├── 48c25f1ad198398cf3f478f942c22afe52460158.nq.gz
│   ├── 4b7b6fd42a6a22118d5e14434f1534b90b47008a.nq.gz
│   ├── 557e727ffdda59180bd7b8ca9ae0203977a49ada.nq.gz
│   ├── 67f486fdfacb0db3d51382bf48d75b3c076eb384.nq.gz
│   ├── 703aced5882ecc6fc1dfd5ed59b34935e1f7e211.nq.gz
│   ├── 7bc1229ab57a4675a2c9559dbd303ce5fe812e5e.nq.gz
│   ├── 97f403ea101384c74ee7273669366de657ee48cd.nq.gz
│   ├── bcc92826c506efec69d298e0d47f50a0b437c958.nq.gz
│   ├── d192a2822735439033fbfaadfc6466fd3aef7e4b.nq.gz
│   ├── d4bf9ca4d7a5649305fdf3197c03b61c76e0c879.nq.gz
│   ├── dbc2e7bf25e612119fb8c04a24dda6ea36e379ec.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── ec10bdc2258e46e39844f9671c2e2caf3795a1e5.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 16b39d2b8ec7500d566ff8b45576ea866d2c719c.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 31 files
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

[pytest-dev/pytest-metadata](https://github.com/pytest-dev/pytest-metadata)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
