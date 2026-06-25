# 🧭 Carbon Compass

**An AI-powered personal carbon footprint tracker — built for SDG 13: Climate Action**

Carbon Compass turns five minutes of everyday lifestyle inputs (travel, electricity, diet, flights, waste) into a single, localized carbon footprint reading — then uses a rule-based AI recommendation engine to tell you exactly which change would reduce your footprint the most, instead of generic "go green" advice.

> 🎓 Built as an AI / Web Development capstone project addressing UN Sustainable Development Goal 13 (Climate Action).

---

## ✨ Features

- **Instrument-panel input form** — sliders & dropdowns for transport, electricity, diet, flights, and waste, with localized electricity grid presets (India grid, global average, renewable-heavy, USA).
- **Carbon Dial** — a custom SVG radial gauge showing your total annual footprint against three reference lines: your 1.5 °C-aligned target, the India average, and the global average.
- **Category breakdown** — animated bars showing exactly how much each category contributes, in kg CO₂e and %.
- **AI recommendation engine** — ranks your top emission sources and generates specific, quantified actions (e.g. *"saves ≈280 kg CO₂e/year"*).
- **Ask the Compass** — a conversational assistant that answers natural-language questions about *your own* results.
- **Goal-setting & trend log** — set a reduction target, save readings to your browser's local storage, and track a trend line over time.
- **100% client-side & private** — no server, no network calls, no data leaves your device. Works completely offline once the page is loaded (aside from optional Google Fonts).

## 🚀 Getting started

No installation, build step, or server required.

1. Download / clone this repository.
2. Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari).
3. Move the sliders, pick your diet and grid, and click **Calculate footprint →**.

```bash
git clone https://github.com/<your-username>/carbon-compass.git
cd carbon-compass
open index.html      # macOS
# or just double-click index.html on Windows/Linux
```

## 🧮 Methodology

Emission factors are approximate, illustrative averages compiled from publicly available references (Our World in Data, UNEP Emissions Gap Report, EDGAR/JRC, IEA, UK DEFRA conversion factors). This is an educational prototype, **not** a certified carbon audit tool.

| Reference line | Value | Source basis |
|---|---|---|
| 1.5 °C-aligned individual target | ≈ 2.3 t CO₂e / year by 2030 | Widely cited "fair share" climate target research |
| India per-capita average | ≈ 2.2 t CO₂ / year | Global Carbon Project / Our World in Data |
| Global per-capita GHG average | ≈ 6.4 t CO₂e / year | UNEP Emissions Gap Report |

## 🛠️ Tech stack

- HTML5, CSS3 (custom properties, Grid), Vanilla JavaScript — no frameworks, no build tools
- Hand-built SVG for the gauge, bar charts, and trend sparkline (no charting library dependency)
- Rule-based recommendation + intent-matching engine for the "AI" layer
- Browser `localStorage` for the reading log
- Google Fonts: Fraunces, Inter, JetBrains Mono

## 📂 Project structure

```
carbon-compass/
├── index.html      # entire application (markup + styles + logic)
├── README.md
└── LICENSE
```

## 🔭 Future scope

- Swap the rule-based assistant for a true generative model (Anthropic/OpenAI API) via a thin backend
- More granular emission factors (vehicle/fuel type, live regional grid-mix data)
- Auto-fill travel data via Maps/transit APIs instead of manual sliders
- Native mobile app with reminders
- Classroom/office group challenges with opt-in shared leaderboards
- Multi-language support
- Exportable PDF footprint report

## 📄 License

MIT — see [LICENSE](LICENSE).
