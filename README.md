# 🌿 Khan's Midnight Healing Rotations

> **Mistweaver Monk** · **Preservation Evoker**  
> Built for Midnight
> Sourced from [Icy Veins](https://www.icy-veins.com) · [Wowhead](https://www.wowhead.com) · SimC APL · Live testing

---

## 📦 Rotations

| File | Spec | Version | Hero Talent |
|------|------|---------|-------------|
| `Khan_Mistweaver_Monk.yaml` | Mistweaver Monk | v1.10.1 | Conduit of the Celestials |
| `Khan_Pres_Evoker.yaml` | Preservation Evoker | v1.8.8 | Chronowarden / Flameshaper |

---

## 🧘 Mistweaver Monk — v1.10.1

An active, mobile healer built around the **Conduit of the Celestials** hero talent tree. Prioritizes Yu'lon's blessings, efficient mana usage, and seamless AoE ramp-up without sacrificing single-target throughput.

### ✨ Highlights

- **Revival** and **Thunder Focus Tea** timed around burst damage windows
- **Renewing Mist** blanketing maintained across the group at all times
- **Rising Sun Kick** integrated to keep the Teachings of the Monastery buff rolling for Vivify cleave
- **Celestial Conduit** burst window synced with trinket usage via `trinket_1.sync`
- Smart **AoE dispatch** via `state.aoe` — switches seamlessly between single-target and multi-target healing
- **Cooldown toggle** support via `state.cds` for manual override
- Trinket usage defaults to **With Major Cooldowns** for maximum burst alignment

### ⚙️ Config Sliders

| Setting | Default | Description |
|---------|---------|-------------|
| Hero Talent Build | Conduit of the Celestials | Selects the active talent tree logic |
| Trinket Usage | With Major Cooldowns | Controls trinket firing window |
| Life Cocoon HP | Configurable | Emergency shield threshold |
| Vivify HP Threshold | Configurable | Single-target heal trigger |
| AoE Member Count | Configurable | Minimum injured players to enter AoE mode |

---

## 🐉 Preservation Evoker — v1.8.8

A deep, technically refined healing rotation built for the **Chronowarden** and **Flameshaper** hero talent paths. Features full empower spell management, Echo duplication sequencing, and extensive self-healing safeguards — refined.

### ✨ Highlights

- **Dream Breath** empowered to the correct stage based on group health — with `empower_releases` for the mandatory second-press trigger
- **Echo** pre-cast before Dream Breath and Reversion so duplications fire on major heals
- **Reversion** used as spread dmg mitigation and healing
- **Verdant Embrace** and **Emerald Blossom** gated behind configurable HP thresholds
- `group.tanks.lowest.range>0` guard on Dream Breath prevents false-firing when no tank is present

### ⚙️ Config Sliders

| Setting | Default | Description |
|---------|---------|-------------|
| Hero Talent Build | Chronowarden / Flameshaper | Selects active talent path logic |
| Trinket Usage | With Major Cooldowns | Controls trinket firing window |
| Deep Breath Enabled | Checkbox (On) | Toggle Deep Breath on/off |
| Emerald Blossom HP | Configurable | HP% threshold to cast Emerald Blossom |
| Verdant Embrace HP | Configurable | HP% threshold to cast Verdant Embrace |

### 🐛 Known Issue

> None currently

---

*Made with way too many `/reload`s.* 🎮
