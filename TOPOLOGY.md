<!-- SPDX-License-Identifier: PMPL-1.0-or-later -->
<!-- Copyright (c) 2026 Jonathan D.A. Jewell (hyperpolymath) <j.d.a.jewell@open.ac.uk> -->

# TOPOLOGY.md — linguist

## Purpose

Linguist is a fork/mirror of [github/linguist](https://github.com/github/linguist), the language detection library used on GitHub.com. It detects blob languages, ignores binary/vendored files, suppresses generated files in diffs, and generates language breakdown graphs. This mirror enables hyperpolymath ecosystem integration and custom enhancements.

## Module Map

```
linguist/
├── lib/              # Ruby library code (language detection, matchers)
├── test(s)/          # Test suite (specs, fixtures)
├── bin/              # Command-line tools
├── docs/             # Documentation (how-linguist-works, overrides, troubleshooting)
├── vendor/           # Dependencies and language grammars
├── samples/          # Language samples for detection training
└── .github/          # GitHub Actions workflows (CI)
```

## Data Flow

```
[Source Code File] ──► [Encoding Detection] ──► [Grammar Matching] ──► [Language Classification]
                                                       ↓
                                              [Override Rules] ──► [Language Breakdown]
```

## Key Integration Points

- **Hyperpolymath ecosystem**: Custom language detectors for emerging DSLs (7-Tentacles, K9, etc.)
- **CI workflows**: RSR standard workflows (hypatia-scan, codeql, quality checks)
- **Contractiles**: Declarative build orchestration via `contractile.just`
