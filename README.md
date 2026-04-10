# Repolex Knowledge Graph of swc-project/jest

RDF knowledge graph data for [swc-project/jest](https://github.com/swc-project/jest), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download swc-project/jest
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ed4e70a9014d827af288e0f16392c7d026f74f86
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── ed4e70a9014d827af288e0f16392c7d026f74f86.nq.gz
│   └── repolex
│       └── ed4e70a9014d827af288e0f16392c7d026f74f86
│           └── chunk-001.nq.gz
├── blob
│   ├── 23fd35f0e0e708ef622c7d957b9c8bb60c7876eb.nq.gz
│   ├── 2813c820c31266ce380eaa14737dfa07c02cd734.nq.gz
│   ├── 29e846eb87de93d7fb88c1f8efb8ccef9dbc686b.nq.gz
│   ├── 35af44547aca171cbd7f57a56fed8be2c06b12e1.nq.gz
│   ├── 3f9a711915a1333434c60267752b5ac8d8d631b7.nq.gz
│   ├── 4c43fe68f6405ee8c6c641998a414c8fa66b0aba.nq.gz
│   ├── 4cd186d1b0a7ddd652f096f9cc85836670d34955.nq.gz
│   ├── 525846c50dcf991746e0f026eaaff6829a1b6418.nq.gz
│   ├── 653c0322aab8d49fd6b588b897b9f34d7d3a10b4.nq.gz
│   ├── 6ae0913b1d2c21b77280bb1ed5a38885e87ecfc7.nq.gz
│   ├── 7a13abb0b5244de1695267529e6513c781d4e72a.nq.gz
│   ├── 7dc9054d8a3119b8c8be059d49fbb3292cd2d11c.nq.gz
│   ├── 853b47167f385f393b23fd74b982a0651d07f431.nq.gz
│   ├── 89e20164c7317c56af5a9202f1f3413a5a9efdae.nq.gz
│   ├── b2cd40d857c8bbe7d106ce5118c15186b63d177d.nq.gz
│   ├── bf7cdebcb5cb7b1dea4b36db81bc160408c22246.nq.gz
│   ├── cc131cfb534a9acf7dd6958884921576e41e5aa3.nq.gz
│   ├── ce9bbbbb9474c3732c9a8325ff425b64e6a39157.nq.gz
│   ├── d9e5950e9ac873462000a8015d014c9f7e803b9b.nq.gz
│   ├── e8203239c058aac1a10ce9cd00ce9daeacc4b703.nq.gz
│   └── f910d06130bbe057039937d78acd1caed40baf4a.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── ed4e70a9014d827af288e0f16392c7d026f74f86.nq.gz
├── filetree
│   └── ed4e70a9014d827af288e0f16392c7d026f74f86.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 31 files
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

## Source repository

[swc-project/jest](https://github.com/swc-project/jest)

---
*Parsed on 2026-04-10 by [repolex](https://repolex.ai)*
