# Repolex Knowledge Graph of jupyter-server/extension-cookiecutter

RDF knowledge graph data for [jupyter-server/extension-cookiecutter](https://github.com/jupyter-server/extension-cookiecutter), parsed by [repolex](https://repolex.ai).

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
rlex download jupyter-server/extension-cookiecutter
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c03fda1fc878fd873b6482e77e9d34a9977e40b6
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c03fda1fc878fd873b6482e77e9d34a9977e40b6
│           └── chunk-001.nq.gz
├── blob
│   ├── 010824e2dea369fdae163ff00236641c3c92f531.nq.gz
│   ├── 0871de2fe7f14371df71eba73bfdcc8bdc21fa60.nq.gz
│   ├── 1a1efd186ba85e8899162c77d57b319010e94d5a.nq.gz
│   ├── 1d57a5b94dd435303ccd9244897f829ab242ea1f.nq.gz
│   ├── 26ff0d4d93c120daab7c5b09959e5f5d2fd0eeb8.nq.gz
│   ├── 2d352af421a2a63c8264e83877f79497337429a6.nq.gz
│   ├── 4248766df97ca4ec24de4c446d488d180899df72.nq.gz
│   ├── 46999335dee35f55376a589f0b9e7369886054f3.nq.gz
│   ├── 5ab5644ab314f5ffb8ed412195b9b58b6fa4d945.nq.gz
│   ├── 68017e224599fcca7d64957b75b776f7f34164d3.nq.gz
│   ├── 7260ed7fd22beb675705e298577d83a28a60c29b.nq.gz
│   ├── 75960e874787132e901f02fc6ce8466115e3734e.nq.gz
│   ├── 83d1229654d01849c21994177291fa16b0db9bf1.nq.gz
│   ├── 848df527337e12a3f4e384db08cffcca666376fa.nq.gz
│   ├── 8579980566cfab905a5aa1753c80e2fef5e0ce8a.nq.gz
│   ├── 9d7b845eba1462302fb89bb9b6bbcdfb5065facf.nq.gz
│   ├── bdaad8974430486f7fa2b18e79d382e6d56f161b.nq.gz
│   ├── c71b5cc78b05030d360052491dbfb2be7e12eac5.nq.gz
│   ├── cbd920f6b3ba719f191d20703765bdeef260b138.nq.gz
│   ├── d121f6fc6688b95eb230d0645a6d836906966bfa.nq.gz
│   ├── d401445be53b0900b9504dd8de954dcf804d1916.nq.gz
│   ├── d43b5593436f8f21e29a6b45de19ddafe2306f69.nq.gz
│   ├── dc409516f41c0461fdfc6c0093db27190f530d86.nq.gz
│   ├── e22bf8ad91c9ffd1d88430b41c50423ddb02b06c.nq.gz
│   ├── e87a06b947a89043e2a69743ba22a2e89e229ddb.nq.gz
│   ├── ecb24722ab6b9967b6ce6337e67cf4e404969b44.nq.gz
│   └── f73f6318f2cde02e05eb5ec7a8641f087ec232d8.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c03fda1fc878fd873b6482e77e9d34a9977e40b6.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 35 files
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

[jupyter-server/extension-cookiecutter](https://github.com/jupyter-server/extension-cookiecutter)

---
*Parsed on 2026-10-21 by [repolex](https://repolex.ai)*
