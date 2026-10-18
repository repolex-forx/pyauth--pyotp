# Repolex Knowledge Graph of pyauth/pyotp

RDF knowledge graph data for [pyauth/pyotp](https://github.com/pyauth/pyotp), parsed by [repolex](https://repolex.ai).

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
rlex download pyauth/pyotp
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cc156832fa9f3d5af7fb9e4e6b86b29dfc5b69f1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cc156832fa9f3d5af7fb9e4e6b86b29dfc5b69f1
│           └── chunk-001.nq.gz
├── blob
│   ├── 037f1f5297cd5ef8fe0244c599126d7c8b529969.nq.gz
│   ├── 08996d3e066ef70082259bd6c32afff0acded799.nq.gz
│   ├── 13dc6fc30419abaea2c5cfd43c49bbec2b8970e7.nq.gz
│   ├── 13e681786a407c8d09d52a8f9cf5ff767717c10e.nq.gz
│   ├── 16052caa7c98be850132950cb317258c7cab5b88.nq.gz
│   ├── 2588e8500a7bc04da28362b528f4f06c374f79c4.nq.gz
│   ├── 26f8d0eca3de357c9134da8fde01f641014335e2.nq.gz
│   ├── 35c6cc6b392cb7d0a5f922e2afffcc536b6a2386.nq.gz
│   ├── 3be2dd9cdecac75b07e18388e570b90e5c35b40a.nq.gz
│   ├── 4bdd1ec8d7c3949c77fcef5688e4b2aa20b0fe65.nq.gz
│   ├── 6ae4a86bc1c741116f9d7b57ee347467451b4153.nq.gz
│   ├── 6c025ce08bce1464389293b67c91bff5f480ce79.nq.gz
│   ├── 6ecdb7ce8fab5b3d45fb39e9defef0aae88034d8.nq.gz
│   ├── 72c3f068d59120d6cd164932d1de0a56d87977fc.nq.gz
│   ├── 7ccd079e7ca45807c0891903cd0a224f95ebf1a1.nq.gz
│   ├── 9729acdf5604b0d71513917e5f37347893e311dc.nq.gz
│   ├── a33aee0412b1f7ecd127b0e146a69b88c9a1008f.nq.gz
│   ├── b2f058f8ae53739f4570ad038ce281208b79ede5.nq.gz
│   ├── c5afe61f0485052ccd9491c50476f5cb3751f4bb.nq.gz
│   ├── cdd567d5609d93da03003d54069d5cde22ce5f91.nq.gz
│   ├── d4ce561e7216fee417254e70f77aa0d69cb5c903.nq.gz
│   ├── e415f45de30fbe943470fc36c8a7c121015fcdca.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f968c9715175dece94466a587688c935c2ae0fcd.nq.gz
│   └── ff14d8f39b82999f7d3aef5bf9ccb8a10b5e4208.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cc156832fa9f3d5af7fb9e4e6b86b29dfc5b69f1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 33 files
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

[pyauth/pyotp](https://github.com/pyauth/pyotp)

---
*Parsed on 2026-10-18 by [repolex](https://repolex.ai)*
