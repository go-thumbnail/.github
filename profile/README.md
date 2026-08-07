<p align="center"><img src="https://raw.githubusercontent.com/go-thumbnail/brand/main/social/go-thumbnail.png" alt="go-thumbnail" width="640"></p>

<h1 align="center">go-thumbnail</h1>
<p align="center">Pure-Go implementation of the freedesktop.org Thumbnail Managing Standard — no cgo, no external tools.</p>
<p align="center"><a href="https://go-thumbnail.github.io/docs/"><img src="https://img.shields.io/badge/docs-mkdocs--material-0F766E?style=flat-square&logo=materialformkdocs&logoColor=white" alt="docs"></a> <a href="https://go-thumbnail.github.io/"><img src="https://img.shields.io/badge/site-go--thumbnail-14B8A6?style=flat-square" alt="site"></a> <img src="https://img.shields.io/badge/Go-1.26-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go"> <img src="https://img.shields.io/badge/license-BSD--3--Clause-0F766E?style=flat-square" alt="license"></p>

---

## What is this?

`go-thumbnail` is a pure-Go (`CGO_ENABLED=0`) implementation of the
freedesktop.org [Thumbnail Managing Standard](https://specifications.freedesktop.org/thumbnail/latest-single/).
It generates and caches file thumbnails **exactly where and how the standard
prescribes**, so thumbnails it writes are visible to other compliant tools —
file managers, image viewers — and vice-versa.

## Module

| Module | freedesktop specification | What it gives you |
|---|---|---|
| [`thumbnail`](https://github.com/go-thumbnail/thumbnail) | [Thumbnail Managing Standard](https://specifications.freedesktop.org/thumbnail/latest-single/) | Canonical cache under `$XDG_CACHE_HOME/thumbnails/{normal,large,x-large,xx-large}` (128 / 256 / 512 / 1024 px), the required PNG metadata (`Thumb::URI`, `Thumb::MTime`, …), fail markers, and shared-repository handling. |

## Design

- **Pure Go, `CGO_ENABLED=0`** — a single portable module; cross-compiles to a static binary.
- **Spec-faithful cache** — canonical directory layout, PNG `tEXt` metadata and fail-marker semantics, so the cache interoperates with existing desktop tools.
- **100% test coverage** is the bar, error branches included.
- **BSD-3-Clause**.

## Links

- 📖 Docs — <https://go-thumbnail.github.io/docs/>
- 🌐 Site — <https://go-thumbnail.github.io/>
- 🎨 Brand assets — <https://github.com/go-thumbnail/brand>

---
<p align="center"><sub>Branding in <a href="https://github.com/go-thumbnail/brand">go-thumbnail/brand</a>.</sub></p>
