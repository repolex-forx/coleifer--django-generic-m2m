# Repolex Knowledge Graph of coleifer/django-generic-m2m

RDF knowledge graph data for [coleifer/django-generic-m2m](https://github.com/coleifer/django-generic-m2m), parsed by [repolex](https://repolex.ai).

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
rlex download coleifer/django-generic-m2m
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── cb67e1cf7700421761e9c144653ff233300ec611
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── cb67e1cf7700421761e9c144653ff233300ec611
│           └── chunk-001.nq.gz
├── blob
│   ├── 06f56d14656ff19865989ae77737350e955d3b0e.nq.gz
│   ├── 0f1a89ca3e63a1b78472ed23e59664828b6eeb78.nq.gz
│   ├── 1011c0b3ef2d425275ba6b01bea0239e9851760d.nq.gz
│   ├── 16ca9f1897a34c6a4c8bbc67571520c8ed7ef2a6.nq.gz
│   ├── 29fab4b67b00413c6645d5b9c6bb12178398d864.nq.gz
│   ├── 2d9e99f09cbd22e9b277b4b1c5441a6115214281.nq.gz
│   ├── 3c43dcd5fb9aa5652981c19bd5aca4cda4fd9ee2.nq.gz
│   ├── 48f19f49c6621a2283647c40bf38c6e6866abf31.nq.gz
│   ├── 4d44812d8ee46a2cfe4e33cc615793410f5d9230.nq.gz
│   ├── 54b74df41b0beb0ae62b52a2e65d8737ef2c1d4d.nq.gz
│   ├── 554f59010461758062886841064526eee1f98d58.nq.gz
│   ├── 558ba469e8dbb8b90c5243f332344d90dbe84cc0.nq.gz
│   ├── 55eb59ff138ba4fe30840b6946cb61f21bd5b096.nq.gz
│   ├── 5e78ea979ea3846a4602f604e265fc4666beffac.nq.gz
│   ├── 6986bc5c7a153d705bc41063bff3074c85c61d26.nq.gz
│   ├── 7d08dac06d64c9c6147ab8f7e439e0f812fb87c1.nq.gz
│   ├── 7d5916b32006e51ac32e2ec588cdf6e9225ee0ab.nq.gz
│   ├── 850d79c4a18baa2309372d11a4013e14ddc131cc.nq.gz
│   ├── 9121c7c65d0bfe2e0a164a09200adbe695c5ab6b.nq.gz
│   ├── 93120e66c81f4b26c1d40a4b853394b85131e9ed.nq.gz
│   ├── 9ccfc90aba0db612bc2beb3875e08a8c0193ab50.nq.gz
│   ├── ac60d5cab11d1c4a146779fb742d6a1529cf4bfe.nq.gz
│   ├── aec0108944deea77a389996740e66327dc947f42.nq.gz
│   ├── bbd0408285043b12824f7fbdbe984bd927944efa.nq.gz
│   ├── bde3d63fa423039ee2652fdc2526361fc8a853d1.nq.gz
│   ├── bef68ea1b1d3d7f03e7e8f121dd13867d21a8e00.nq.gz
│   ├── bfe8a6c5da3f4502dd467f7e9eb92e3840a33d73.nq.gz
│   ├── c07c44ca13fcb3119555694d57da14c05c587982.nq.gz
│   ├── c174f4ff310c282f2d25276665409ebbe4bd25b4.nq.gz
│   ├── cdefd4e2092d3581615c18d38c685c0c0c3d341d.nq.gz
│   ├── d3d67ae44bb2174ba9ebd5aacb923f18eb6a0741.nq.gz
│   ├── d9df6394d0ab21ca7eca8aea63999f6f11ff03e5.nq.gz
│   ├── daa1dcbc9f4b8be2130181dcd8dcd0ee02f8c175.nq.gz
│   ├── dea108b156c88b828f17566a0431a2bbbe32a85e.nq.gz
│   ├── e210fc378b194319ab422c31c4caa9f5d981bdb4.nq.gz
│   ├── e5b46f9ab54fd7f3b1a8efdb52d1acac2f64dcda.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec1568853be0c2e266430fd995140a9773e488a3.nq.gz
│   └── f0ad175f1ae3c1e0007a2c88f365bf40b7dc3c06.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── cb67e1cf7700421761e9c144653ff233300ec611.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 47 files
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

[coleifer/django-generic-m2m](https://github.com/coleifer/django-generic-m2m)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
