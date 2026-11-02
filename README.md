# Repolex Knowledge Graph of zopefoundation/DateTime

RDF knowledge graph data for [zopefoundation/DateTime](https://github.com/zopefoundation/DateTime), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/DateTime
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b157397e216276ee6fb52ed460465a630d6f308e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b157397e216276ee6fb52ed460465a630d6f308e
│           └── chunk-001.nq.gz
├── blob
│   ├── 045e0ff496870b210f33f2e12dc3b2fbf56f5e01.nq.gz
│   ├── 22568f14c91e1687d0055564f00a65420ff361a1.nq.gz
│   ├── 233772274abd002cac35070bcc1539f4a813dc73.nq.gz
│   ├── 386c3daeb6a8836da3fea100c8ebddc30669bd7d.nq.gz
│   ├── 3ac9a40b77eac0abdffad1125e03955be874274e.nq.gz
│   ├── 3e59c09b5e2f1384f86a6559a10d373b3c865cfa.nq.gz
│   ├── 4acf3248d1817f5f61a5c5b8606e18c4cc2c511d.nq.gz
│   ├── 4bb15cb147945e9d997106890ae2463301ddd699.nq.gz
│   ├── 4e2df6da0547866fc04196d93c13e93891124695.nq.gz
│   ├── 5b3f07df00d9f23516ca3658795aa1b366461503.nq.gz
│   ├── 67fe1fbf166ba7910dfb9c5859259778b6d7adec.nq.gz
│   ├── 7396c7bf2d6cdeec9ecf7fea7e94592e6d38074d.nq.gz
│   ├── 943b1b8180b0decc3c7cea40d145ce1f49191aca.nq.gz
│   ├── 9aea56fa71380082c334d7f1805b6c0e2d6b423d.nq.gz
│   ├── a0c56896dece0960f66bd4e7720b7556a55921a4.nq.gz
│   ├── a128fb906d1482fbbc7b731c965c1d29c48189e5.nq.gz
│   ├── aad785ab8c1e63a58437629ad8a21928d723c763.nq.gz
│   ├── b1844c2862f23ba853d62daf874b298725048415.nq.gz
│   ├── b5a3eff1b670d143adedaa1839976b26fc1aa6ef.nq.gz
│   ├── b70d76cff4b12ab3651fd2fec54b0eafa16ca6ff.nq.gz
│   ├── b8581dd898cbb33e63961b4d181ff0ffbe5d03ee.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e67bcb6769f051b7095d227e0dc9d1f6a72a1b08.nq.gz
│   ├── e6e26dd728ab6d888e3bb330bd363248dfed49d8.nq.gz
│   ├── e7df4ec70f1aa64c04d00512aab46c2afe0fe193.nq.gz
│   └── eed5b4b3c3a18ea8dc1d08ca037add9bdec66f63.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b157397e216276ee6fb52ed460465a630d6f308e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 34 files
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

[zopefoundation/DateTime](https://github.com/zopefoundation/DateTime)

---
*Parsed on 2026-11-02 by [repolex](https://repolex.ai)*
