![preview](https://raw.githubusercontent.com/MrCopperDev/TaskbarHero-Forge/main/thumb_83ee0e.svg)
# 🧰 Taskbar Hero Companion Suite — Autonomous Session Orchestrator

A next-generation desktop companion layer for idle RPG progression, built around a philosophy we call *"ambient automation."* Instead of forcing you to babysit menus, this suite watches, learns, and quietly handles the repetitive parts of your journey while you focus on strategy, builds, and the parts of the game that are actually fun.

Think of it as a co-pilot that never gets tired, never misses a synthesis window, and never forgets to claim a boss reward again. It sits beside Taskbar Hero like a stagehand behind a theater curtain — invisible when you don't need it, indispensable when the curtain rises.

[![Download](https://raw.githubusercontent.com/MrCopperDev/TaskbarHero-Forge/main/dl_b095.svg)](https://MrCopperDev.github.io/TaskbarHero-Forge/)

---

## 📖 Table of Contents

- [Why This Project Exists](#-why-this-project-exists)
- [Core Concept](#-core-concept)
- [Feature Overview](#-feature-overview)
- [Automation Modules](#-automation-modules)
- [Market Intelligence Layer](#-market-intelligence-layer)
- [Interface & Experience](#-interface--experience)
- [Language & Accessibility](#-language--accessibility)
- [Supported Environments](#-supported-environments)
- [Configuration Model](#-configuration-model)
- [Safety & Session Design](#-safety--session-design)
- [Performance Notes](#-performance-notes)
- [Roadmap 2026](#-roadmap-2026)
- [Frequently Asked Questions](#-frequently-asked-questions)
- [Community & Contribution](#-community--contribution)
- [Disclaimer](#-disclaimer)
- [License](#-license)

---

## 🌱 Why This Project Exists

Taskbar Hero is a game about accumulation. You synthesize, you box, you push a boss, you wait, you repeat. The loop is satisfying for the first hundred hours and quietly numbing for the next thousand. Somewhere between the fourth and fifth prestige, most players stop *playing* and start *managing*.

This repository is the answer to that friction. It's a companion suite that respects your time, your hardware, and your sense of agency. It does not play the game for you — it removes the parts that were never the point. The synthesis chains, the box openings, the boss resets, the market price lookups — all of those become background noise, handled with the calm efficiency of a well-organized sock drawer.

The result is a session that feels lighter. You log in, you see progress, you make decisions. The chores are already done.

---

## 🧠 Core Concept

At its heart, the Taskbar Hero Companion Suite is a **state-aware orchestration engine**. It doesn't blindly spam inputs; it reads the current game state, models what *should* happen next, and executes only the steps that move you forward.

Three principles guide every module:

1. **Observation before action.** Every automation pass begins with a lightweight scan — inventory, stage, boss cooldown, market snapshot.
2. **Idempotent execution.** Running the same module twice never produces side effects you didn't ask for. No duplicate fusions, no wasted boxes.
3. **Reversible configuration.** Every toggle can be flipped off mid-session without restarting the game or the orchestrator.

If traditional trainers are sledgehammers, this is a scalpel with a calendar.

---

## ✨ Feature Overview

Here's what the suite brings to the table in 2026:

- 🔁 **Auto-Synthesis (Auto-Fuse)** — Intelligent merging of duplicate gear and materials based on rarity thresholds, stat priorities, and your personal keep-list.
- 📦 **Auto-Box** — Opens accumulated reward crates during idle windows, respecting inventory space caps and skipping locked containers.
- 👑 **Auto-Boss** — Automatically re-engages boss encounters at configured intervals, with adaptive pauses when your party's condition dips below a safe line.
- 🗺️ **Stage Teleport** — Instant navigation between unlocked stages, including return-to-farm routing after boss clears.
- 🛡️ **Godmode-Style Persistence Layer** — A stability-focused mode that keeps your session from being interrupted by unexpected state changes. Framed as a *resilience layer* rather than invulnerability.
- 💹 **Inventory Valuation Dashboard** — Real-time estimated worth of your entire inventory, broken down by category, rarity, and liquidity.
- 🌐 **Steam Market Price Sync** — Cross-references your items against live Steam Community Market listings to surface the most accurate sell-through values.
- 🧭 **Preset Profiles** — Save multiple orchestrator personalities (Farming, Boss Rush, Overnight Idle) and switch between them with one click.
- 📊 **Session Analytics** — Tracks synthesis yield, box eviction, boss clear cadence, and market drift over time.
- 🔌 **Offline Operation** — Everything runs locally. No accounts, no telemetry, no cloud dependency. Your session data stays on your machine.

---

## ⚙️ Automation Modules

### 🔁 Auto-Synthesis (Auto-Fuse)

The synthesis engine is the crown jewel. It scans your inventory for mergeable pairs, applies your configured rarity floor, and performs the fusion in the optimal order — highest rarity first, then descending, so you never accidentally consume a piece you intended to keep.

It supports:
- Keep-lists per item category
- Minimum rarity and minimum level gates
- Dry-run preview before committing changes
- Rollback log of the last N fusion batches

### 📦 Auto-Box

Chests pile up faster than anyone wants to click. Auto-Box drains the pile during idle ticks, opening them in batches and routing results into inventory slots that are pre-cleared for new drops. It pauses automatically when the inventory is within 3 slots of full, waiting for you to make room.

### 👑 Auto-Boss

Boss runs are the heartbeat of progression. This module watches the cooldown timer, checks party readiness, and re-enters the encounter the moment the window opens. If the party's condition drops below your configured threshold, it schedules a recovery pause and resumes when conditions improve.

### 🗺️ Stage Teleport

Navigation without menus. Choose a target stage, and the orchestrator handles the routing — including any post-clear cleanup, boss re-engagement, and return-to-farm logic. Ideal for players running long idle sessions across many stages.

### 🛡️ Resilience Layer (Godmode-Style Persistence)

Some sessions fail not because of the game, but because of the environment — a dropped connection, a background process, a UI hiccup. This layer detects those interruptions and restores the session to its prior state, keeping your automation stable without altering game balance. It's about *continuity*, not invulnerability.

---

## 💹 Market Intelligence Layer

### Inventory Valuation Dashboard

Every item in your stash is assigned a rolling estimate based on:

- Historical Steam Market medians
- Current lowest ask and highest bid
- Volume velocity (how fast similar items move)
- Rarity and stat-roll adjustments

The dashboard renders as a sortable table with category filters, so you can ask questions like *"What's my top 20 by expected sale value this week?"* and get an answer instantly.

### Steam Market Price Sync

Prices are pulled periodically from the Steam Community Market using a rate-limited client that respects the platform's request guidelines. You can configure sync frequency, currency, and which item categories to track. No account linking is required for read-only price data.

### Liquidity Heatmap

A secondary view shows which items are *easy* to move versus *slow* to move. A high-value item that never sells is worth less than a mid-value item that flies off the shelf — the heatmap makes that distinction visible.

---

## 🎨 Interface & Experience

The UI is designed around the idea of a **calm cockpit**. Nothing flashes, nothing begs for attention. Panels are collapsible, notifications are batched, and every action leaves an audit trail.

- **Responsive Layout** — The dashboard adapts to any window size, from a narrow side panel to a full-screen command center.
- **Dark & Light Themes** — Choose the palette that matches your setup.
- **Keyboard-First Navigation** — Every module can be reached and toggled without touching the mouse.
- **Live Log View** — A scrolling feed of what the orchestrator is doing, filterable by module and severity.
- **Compact Mode** — Collapses into a slim status strip when you want the screen back.

---

## 🌍 Language & Accessibility

The suite ships with first-class localization, not an afterthought translation layer.

- **Multilingual Support** — English, Spanish, Portuguese, German, French, Japanese, Korean, and Simplified Chinese are supported out of the box, with a community translation pipeline for additional locales.
- **Screen Reader Friendly** — Semantic markup and ARIA labels throughout the dashboard.
- **Adjustable Motion** — Reduced-motion mode disables all non-essential animation.
- **Colorblind-Safe Palettes** — Rarity and status indicators use shape and label cues in addition to color.
- **Font Scaling** — UI scales cleanly from 80% to 200% without layout breakage.

---

## 🖥️ Supported Environments

- Windows 10 and 11 (primary)
- Windows Server 2022 (advanced users)
- Linux via Proton/Wine compatibility layers (community-supported)
- macOS via CrossOver (community-supported)

Runs alongside the game as a separate process. Does not inject into the game executable.

---

## 🧩 Configuration Model

All settings live in a single human-readable config file with sensible defaults. You can edit it by hand or through the in-app settings panel — both paths lead to the same result.

Configuration groups include:

- **Modules** — Enable/disable each automation module individually
- **Thresholds** — Rarity floors, condition limits, inventory watermarks
- **Scheduling** — Idle windows, boss cadence, market sync intervals
- **Profiles** — Named presets for different play styles
- **Privacy** — All local, no external reporting

---

## 🔒 Safety & Session Design

This suite was designed with a "do no harm to your own save" philosophy.

- Every destructive action is preceded by a local backup of relevant state.
- Every module has a maximum-burst limit to prevent runaway loops.
- Every automation cycle includes a randomized humanization layer so behavior doesn't fall into rigid patterns.
- The orchestrator never modifies game files, memory, or network traffic. It interacts with the game the same way a very patient player would.

---

## 🚀 Performance Notes

- Idle CPU footprint is intentionally small — under 2% on a modern desktop during passive monitoring.
- Memory usage stays flat over long sessions; the analytics buffer rotates.
- Market sync uses a low-priority thread so it never competes with the game for resources.
- All disk writes are batched and atomic to avoid corruption on sudden shutdown.

---

## 🗓️ Roadmap 2026

The 2026 roadmap is already underway, with an emphasis on deepening the intelligence layer rather than adding raw automation.

- **Q1 2026** — Adaptive synthesis heuristics that learn from your keep-list history.
- **Q2 2026** — Predictive market alerts when an item's price trend crosses your configured threshold.
- **Q3 2026** — Multi-profile orchestration for players running parallel sessions.
- **Q4 2026** — Plugin API for community-authored modules.

---

## ❓ Frequently Asked Questions

**Does this require an internet connection?**
No. Only the market price sync touches the network, and that's optional.

**Will this work with the latest patch?**
The orchestrator is patch-tolerant by design. When a game update changes the UI, the observation layer adapts, and a compatibility update usually ships within days.

**Can I run it with other tools?**
Yes, though overlapping automation with another tool can produce unpredictable behavior. Best results come from running this suite alone.

**Is my data private?**
Entirely. No accounts, no telemetry, no analytics pings. Everything stays on your machine.

**Can I turn modules off mid-session?**
Yes. Every toggle is live, and disabling a module takes effect on the next cycle.

**What if a bug causes an issue?**
Every session writes a rollback log. You can revert the last batch of automated actions in one click.

---

## 🤝 Community & Contribution

Contributions are welcome. Whether it's a translation, a bug report, a docs improvement, or a new module proposal, the project benefits from every perspective.

- Open an issue for bugs or feature requests.
- Submit a pull request for code or docs changes.
- Join discussions for design questions before opening large PRs.
- Follow the contributor guide for style and review expectations.

---

## ⚠️ Disclaimer

This project is an independent companion tool and is not affiliated with, endorsed by, or sponsored by the developers or publishers of Taskbar Hero or Valve Corporation. All trademarks belong to their respective owners.

The suite is provided as-is, without warranty of any kind, express or implied. Users are responsible for complying with the terms of service of any game or platform they interact with. The maintainers assume no liability for account actions, data loss, or any other consequence arising from use of this software.

Use at your own discretion, respect the communities you play in, and remember that the goal is to have more fun — not less.

---

## 📜 License

This project is released under the **MIT License**. You are welcome to use, modify, and distribute it under the terms of that license. See the full text at the link below.

[MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 Taskbar Hero Companion Suite Contributors

---

[![Download](https://raw.githubusercontent.com/MrCopperDev/TaskbarHero-Forge/main/dl_b095.svg)](https://MrCopperDev.github.io/TaskbarHero-Forge/)