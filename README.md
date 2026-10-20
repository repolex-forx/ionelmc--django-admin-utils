# Repolex Knowledge Graph of ionelmc/django-admin-utils

RDF knowledge graph data for [ionelmc/django-admin-utils](https://github.com/ionelmc/django-admin-utils), parsed by [repolex](https://repolex.ai).

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
rlex download ionelmc/django-admin-utils
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 11f1ab96031ef08ace0ee42f5a2c1adac8b2bcac
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 11f1ab96031ef08ace0ee42f5a2c1adac8b2bcac
│           └── chunk-001.nq.gz
├── blob
│   ├── 017190489850a804e5acaacda3c35f9400a1678f.nq.gz
│   ├── 05c286fa72e82e9be644940e12c88b63a09277aa.nq.gz
│   ├── 08936d99094e1b728f76a1a13bc81ce1cdbe0cb7.nq.gz
│   ├── 1dd5342070a683dab0f891a83dc68978cee86f97.nq.gz
│   ├── 22d590b0b170973a19746adaad7cc0c5d0891280.nq.gz
│   ├── 38d05b6ad37a1caffeb26f89cc5f8d09e52c95fc.nq.gz
│   ├── 49e39a8f77fd6d49094502737913e0a2235b5607.nq.gz
│   ├── 4da56772ccfa130d07f9ffb78af84fbe897ecc5f.nq.gz
│   ├── 6c4b9701dd53db3bb71c04b3fa7193d4390e3988.nq.gz
│   ├── 780c7edb823d789b0d5d336e0ba76dd225a5213a.nq.gz
│   ├── 7ad21bb327114d298ff12383a80d7d898f7e40cc.nq.gz
│   ├── 83269803ce07937e7cc672a8560dc876d4893932.nq.gz
│   ├── 8569bb60ff03c13b06b8ad18cba0b95858b7ca64.nq.gz
│   ├── 8b5b73c8d42c94274dfc3cf43dbddeff6bdee010.nq.gz
│   ├── 8f8054d37b6daa5aacc507f0e5907b86d0de3d6f.nq.gz
│   ├── 8faaf6634147dac7dd44ba25cd32837472c7f2fd.nq.gz
│   ├── 91cf2087b70434656b28031d2c247de3d291bb42.nq.gz
│   ├── 92439c0809e5a99d31d57afb9a26647ab109db72.nq.gz
│   ├── 92c6aa549ca12dfb46ead545a24bcd87fc951ce4.nq.gz
│   ├── 93f199653700c37e6b401d190e977e2c855a419a.nq.gz
│   ├── 940e652a2ed2735b1d66988d10ce1865362e4d69.nq.gz
│   ├── 960b88239927f999dd37f270cfd7e5899a42e1fe.nq.gz
│   ├── 98d0cc767e7d51c4897850f500aeaed20ba6244f.nq.gz
│   ├── a2f4598357e02cd53bcc8c735b0afd8a9121ef54.nq.gz
│   ├── b261eff2c30f38d67a90a3df2fb581bbd43d3e3b.nq.gz
│   ├── b45e6a65103e1e08cb7b1f87f5f760eaef37f740.nq.gz
│   ├── c1a280731498687c7c31c989352de02af0ada697.nq.gz
│   ├── c88b94378995a059f6dc7c13c1f3b261a575c5f1.nq.gz
│   ├── d01607af0a29bbccb70ed3e82bdfdce51fd6e02e.nq.gz
│   ├── d069fb52fc7f5bb5a00119116997130995ae5e97.nq.gz
│   ├── de849b4de21208d4bf161d71125e250822a31d4c.nq.gz
│   ├── e0b2f5b105102344f20b6fdf02fe093edd07197f.nq.gz
│   ├── e161c09e71a7a8edf7bcc43205c0a5c761160eeb.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f913a4c4f71fa47fbd7775bf6fb4253e2e075896.nq.gz
│   ├── fa7a4b2845213e13d2bc83c83b8e4f106a7f7a7f.nq.gz
│   └── fe36036bc549b4deeb1a7291efc3e66baaf86cf8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 11f1ab96031ef08ace0ee42f5a2c1adac8b2bcac.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 44 files
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

[ionelmc/django-admin-utils](https://github.com/ionelmc/django-admin-utils)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
