# Does a Solar-Powered Air Conditioner Help or Hurt the Climate?

> **Counter-intuitive finding:** When powered by rooftop solar panels and assessed
> across its entire lifespan — including manufacturing carbon and expected refrigerant
> leakage — a residential air conditioning unit is a **net carbon sink**.
> The behavioural carbon emissions it prevents (extra showers, laundry, refrigerator
> overwork, accelerated device degradation) outweigh its full annualised lifecycle
> footprint by a comfortable margin.

---

## What This Repository Contains

A complete, sustainability assessment of a real residential
installation in Basel, Switzerland — from raw data and methodology through to a
published lay briefing, technical report, and visual infographic.

| File | Description |
|---|---|
| `Solar AC Climate Benefit Methods and Results.pdf` | Detailed technical report |
| `index.html` | Self-contained A4 infographic (open in any browser) |

---

## The System Assessed

- **Unit:** Daikin Stylish FTXA50/RXA50 split air conditioner
- **Refrigerant:** R-32 (1.30 kg factory charge)
- **Location:** Basel, Switzerland — residential building constructed 1999/2000
- **Energy source:** 100% on-site rooftop photovoltaic generation on cooling days
- **Indoor setpoint:** 22.0 °C (owner-confirmed)
- **Operational pattern:** Physically disconnected from the grid October through April,
  eliminating all winter standby carbon

---

## The Key Finding
C_net = −35 − 6.6·S kg CO₂e per year


Where **S** is the daily solar surplus exported to the grid (kWh/day).

At zero export (S = 0), the system is already net carbon-negative by **35 kg CO₂e/year**.
At a modest export of 10 kWh/day, the benefit reaches **−101 kg CO₂e/year**.

| Annual carbon cost of owning the system | 43 kg CO₂e/yr |
|---|---|
| Annual carbon avoided through human behaviour | **78 kg CO₂e/yr** |
| **Net position before any solar export credit** | **−35 kg CO₂e/yr** |

The 15-year cradle-to-grave lifecycle carbon footprint is **651 kg CO₂e** — equivalent
to driving a small petrol car approximately 4,500 km, for 15 years of summer cooling.

---

## What Drives the Net-Negative Result

Most lifecycle assessments of air conditioners ask only: *what carbon does the unit emit?*
This assessment also asks: *what carbon would the household emit without it?*

When a home has no active cooling during a 39 °C Basel heatwave, residents adapt —
and those adaptations have measurable carbon consequences:

| Behavioural Effect | Avoided Carbon |
|---|---|
| Extra heat-relief showers (gas boiler water heating, 4 persons) | 55 kg CO₂e/yr |
| Additional laundry cycles and accelerated textile wear | 21 kg CO₂e/yr |
| Ground-floor Miele refrigerator overwork (IEC 62552 calibrated) | 1 kg CO₂e/yr |
| Accelerated electronic device degradation (Arrhenius chemistry) | 1 kg CO₂e/yr |
| **Total avoided behavioural carbon** | **78 kg CO₂e/yr** |

> The basement Liebherr GNP 3166 freezer is **correctly excluded** from this calculation:
> its basement environment (16–20 °C year-round from ground thermal mass) is thermally
> independent of the air conditioning system.

---

## Methodology

| Element | Approach |
|---|---|
| **Lifecycle boundary** | EN 15978 (modules A1–A5, B1, B6, C1–C4, Module D) |
| **Climate metric** | IPCC Sixth Assessment Report (AR6) GWP100 |
| **Building physics** | SIA 382/1 four-path thermal load; MeteoSwiss BAS hourly data |
| **COP derivation** | Independent diurnal load integration (non-circular); Rule 9 Second Law check |
| **Refrigerant lifecycle** | Compound remaining-charge EOL arithmetic; SENS eRecycling statistics |
| **Standby carbon** | Daytime/nighttime split; Oct–Apr disconnection confirmed zero |
| **Appliance data** | IEC 62552-3:2015 sensitivity (4.5%/K); Miele and Liebherr datasheets |
| **Citations** | 32 primary sources; all from IPCC, IEA, ASHRAE, MeteoSwiss, IEC, or peer-reviewed journals |

### Generation Pipeline

This assessment was produced using a **two-stage AI pipeline** designed to separate
data retrieval from numerical modelling:

1. **Stage 1 — Gemini Deep Research:** Structured data extraction from primary sources
   (IPCC, MeteoSwiss, Daikin technical databooks, ÖKOBAUDAT, peer-reviewed LCA literature).
   Output: a verified data repository with source tags and uncertainty bounds.

2. **Stage 2 — Claude Sonnet:** Lifecycle modelling, thermal load calculations, and
   report generation using only the Stage 1 repository as input. No training-memory
   substitution permitted; all gaps flagged explicitly as [MISSING INPUT] or [APPROXIMATED].

This architecture separates citation retrieval (where LLMs are strong) from arithmetic
consistency (where they historically fail), producing measurably better internal
consistency than single-prompt approaches.

---

## Key Limitations

- No product-specific EPD exists for the Daikin FTXA/RXA series; embodied carbon
  (439 kg CO₂e, ±25%) is estimated from peer-reviewed LCA literature
- The daily PV export surplus **S** is unmetered; all Module D calculations are
  parametric functions of S
- Household occupancy (4 persons) and behavioural response assumptions contribute
  ±45% composite uncertainty to the behavioural carbon total
- Standby power (estimated 26.5 W combined) carries ±50% uncertainty as the
  stator heating specification could not be confirmed from a publicly accessible document
- The single largest controllable risk is **refrigerant leak rate**: the difference
  between best-practice (0.5%/yr) and EU-default (5.0%/yr) leakage is
  **541 kg CO₂e over 15 years** — greater than the entire equipment embodied carbon

---

## Sources

All quantitative claims are traceable to primary sources. Key references:

- IPCC AR5 WGI Chapter 8 Table 8.SM.16 (GWP values)
- IPCC AR6 WGI Chapter 7 Table 7.SM.7 (GWP values)
- MeteoSwiss Basel-Binningen station BAS (climate data)
- Daikin Technical Databook EEDEN18, RXA-B series
- SIA 380/1:1988 (Swiss building insulation standard)
- AIVC Airbase Paper 13390 (staircase natural convection)
- IEC 62552-3:2015 (refrigerator ambient temperature sensitivity)
- ASHRAE HVAC Systems and Equipment Handbook, 2020, Chapter 37
- SENS eRecycling Fachbericht 2024 (Swiss EOL refrigerant recovery)
- EU F-Gas Regulation 2024/573, Article 2
- ÖKOBAUDAT Process Dataset for Difluoromethane R-32
- International Journal of Refrigeration (R-32 solubility in POE lubricant)

Full citation audit table with compliance status available in the technical report (Appendix B).

---

## Licence

This work is released under the **Creative Commons Attribution 4.0 International
(CC BY 4.0)** licence. You are free to share and adapt this material for any purpose,
provided appropriate credit is given.

---

## Contact

Assessment commissioned and conducted independently.
Basel, Switzerland · 2025–2026

*Generated using a two-stage AI research and modelling pipeline with mandatory
source verification, internal consistency audit, and independent technical review.
All conclusions have been audited against primary scientific sources.*
