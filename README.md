# ChronoWeather 🌍🛰️  
**NASA-powered climate intelligence for event planning, safety, and reproducible open-data reuse.**

ChronoWeather is an open-source Android application (Kotlin) that transforms NASA Earth observation and climate archives into **actionable, explainable, and reproducible weather + climate insights** for real-world planning.  
Instead of showing only a short-term forecast, ChronoWeather answers:

> **“What will it feel like, what are the risks, and what historically happened in similar years?”**

It is built for **Indian weather volatility** (heatwaves, sudden rainfall, monsoon uncertainty, cyclones) and supports **transparent provenance** with LIVE/CACHED/SIMULATED data modes so the app stays functional even under API/quota failures.

---

## 🚀 Key Highlights
- **Analog Year Finder**: Finds historical years with the most similar climate fingerprint to your event date.
- **Route Weather Simulator**: Minute-by-minute risk projection across checkpoints along your route.
- **Comfort Score + Activity Risk**: Converts raw climate variables into decision-grade comfort and risk guidance.
- **NASA Data Hub**: Explore datasets with citations, metadata, and export support.
- **Ground Truth Validation**: Combines satellite context + local reports to improve trust.
- **Open-Source + Reusable**: Evidence exports, schemas, and documentation for public reuse.

---

## 🎯 Problem Statement (Indian Context)
India is facing increased climate variability: heatwaves, cloudbursts, extreme rainfall, and unpredictable seasonal shifts.  
Citizens, MSMEs, outdoor workers, event organizers, and local communities often rely on generic weather apps that:

- focus only on short-term forecasts
- do not explain uncertainty or risk clearly
- do not provide historical analog context
- do not expose reproducible datasets for public reuse

Meanwhile, NASA provides world-class open climate archives (MERRA-2, GPM, MODIS), but these datasets are not easily usable for decision-making without significant preprocessing and expertise.

ChronoWeather bridges this gap by converting raw NASA archives into **AI-ready insights**, with **transparent provenance** and **reproducibility-first design**.

---

## 🧠 How ChronoWeather Works (High Level)
ChronoWeather follows a simple and robust flow:

1) **User selects location + date + activity type**
2) App fetches climate variables from NASA datasets (LIVE mode)
3) If live retrieval fails, app falls back to:
   - **CACHED NASA snapshots** (verifiable and versioned)
   - **SIMULATED deterministic patterns** (last-resort continuity)
4) The system generates:
   - analog year matches
   - 7-day event timeline
   - route simulation with checkpoint risks
   - comfort and risk scoring
5) Every output includes:
   - dataset citations
   - provenance mode
   - reproducibility evidence export

---

## ✅ Core Features
### 1) Analog Year Finder 🎯
Matches a “climate fingerprint” for your event date against historical NASA records to find similar years.

### 2) 7-Day Weather Timeline 📅
Day-by-day planning view (3 days before → event day → 3 days after) with comfort ratings.

### 3) Route Weather Simulator 🗺️
Minute-by-minute weather and risk projections across checkpoints along your route.

### 4) Ground Truth Validation 🛰️
Shows satellite context + enables crowdsourced local condition reporting.

### 5) Global Climate Connections 🌍
Explains how large-scale indices (ENSO/IOD/NAO where applicable) relate to local conditions.

### 6) NASA Data Hub 📊
Explore NASA datasets with interactive charts and downloads.

### 7) AR Weather Replay 📸
Augmented reality overlay showing historic weather events at the user’s location.

### 8) Community Storyboard 💬
Users share real experiences from analog years (e.g., marathon/wedding planning tips).

### 9) Comfort Score 🌡️
A 0–100 comfort score for event conditions.

### 10) Activity Risk Assessment ⚠️
Risk warnings for specific activities (marathon, outdoor work, weddings, farming, etc.)

### 11) Multi-Format Export 💾
Exports as PDF / CSV / JSON.

### 12) Historical Forecast Library 📚
Stores and compares previous searches.

### 13) Learning Hub 🎓
Explains climate science, satellites, and dataset interpretation.

### 14) AI Transparency Report 🤖
Explains how AI is used, what data was used, and limitations.

### 15) Impact Dashboard 🌟
Shows usage and success metrics (prototype dashboard).

---

## 🧩 Open-Source + Public Reuse Features
### Data Provenance Tracking 🔍
Every result is labeled:
- **LIVE** (real-time NASA retrieval)
- **CACHED** (versioned NASA snapshot)
- **SIMULATED** (deterministic fallback)

### Reproducibility Export 📥
Download a full JSON evidence file containing:
- query parameters (location, date, activity)
- datasets used + citations
- snapshot IDs + checksums
- pipeline steps
- output hashes

### Reproducibility Score (0–100)
A measurable score based on:
- data completeness
- validation checks
- source mode quality

### Dataset Cards 📖
Each chart includes citation-grade metadata:
- DOI / dataset reference
- variables
- resolution
- update frequency

### Data Sources Page
Full catalog of datasets used with attribution and access methods.

### Reuse Portal (Developer Hub)
Includes:
- JSON schemas
- sample payloads
- export examples
- integration guidance

### Evidence Mode (Judge-Friendly)
Dashboard showing:
- API status
- fallback counts
- provenance breakdown
- snapshot registry

### Offline Mode
Download a cached snapshot bundle to keep functionality in low connectivity or quota failures.

---

## 📊 Validation Report
ChronoWeather includes an in-app **Validation Report** screen that verifies:
- API health monitoring (NASA endpoints)
- data integrity checks (missing values, ranges, continuity)
- reproducibility verification (hash matching)
- schema validation status
- system reliability score breakdown

It also supports **Validation Evidence Export** as JSON for judge verification.

---

## 📚 Data Sources
ChronoWeather uses NASA open datasets including:

- **NASA MERRA-2 (GES DISC / Giovanni)**  
  Reanalysis climate variables (temperature, humidity, wind, etc.)

- **NASA GPM (Global Precipitation Measurement)**  
  Satellite precipitation estimates

- **NASA MODIS (Terra/Aqua)**  
  Satellite imagery and derived products (cloud cover, land surface indicators)

- **NASA Worldview / Giovanni**  
  Access portals for visualization and data discovery

> Exact dataset metadata, DOI/citations, and access details are available in-app under **Data Sources** and per-chart **Dataset Cards**.

---

## 🔐 Licensing
### Code License
This project is released under the **MIT License**.  
See [`LICENSE`](./LICENSE).

### Data Licensing / Attribution
NASA Earth science datasets are generally open-access, but each dataset may have specific citation requirements. ChronoWeather provides dataset attribution through:
- Dataset Cards
- Data Sources Page
- Evidence Exports

---

## 🛠️ Tech Stack
- **Platform:** Android (Kotlin)
- **UI:** Jetpack Compose / XML (depending on implementation)
- **Data layer:** NASA dataset connectors + snapshot registry + deterministic fallback simulator
- **Exports:** JSON / CSV / PDF (implementation dependent)

---

## ▶️ Setup & Run (Android Studio)
1) Clone the repository:
```bash
git clone <https://github.com/shreyabj/ChronoWeather--AI-For-All.git>
cd ChronoWeather
