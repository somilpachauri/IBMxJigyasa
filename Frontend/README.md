# 🌐 NH7 Raah — Web Dashboard & Control Center

Interactive web platform for real-time landslide monitoring, safer route planning, ground incident reporting, and emergency resources along the NH-7 highway corridor (Rishikesh to Badrinath/Joshimath, Uttarakhand). Built for the **IBM x Jigyasa Hackathon 2026**.

---

## 🚀 Overview

The frontend serves as the primary traveler portal and administrative operations console:
- **Interactive Live Map**: Real-time Leaflet map displaying 18 highway segments color-coded by AI-calculated landslide hazard levels (Low, Moderate, High, Severe, Closed).
- **Time-Aware Trip Planner**: Analyzes route segments with arrival ETAs, warns of impending rainfall peaks, and recommends alternative ML departure windows.
- **Bilingual Interface**: Full support for English and Hindi (हिन्दी) across all labels, town names, and risk verdicts.
- **Neural Voice Alerts**: In-browser streaming of bilingual voice advisories (`GET /voice-alert?lang=hi`).
- **Ground Incident Reporting**: Community-driven reporting of rockfalls, debris, roadblocks, and weather hazards with photo upload capabilities.
- **Offline Emergency Hub**: One-tap access to emergency helplines, nearest hospitals, SDRF/NDRF contacts, and cached offline hazard packs.
- **Rainfall Simulation Studio**: Interactive testing modal to simulate extreme rainfall scenarios (0 mm – 180 mm) and observe instantaneous corridor risk shifts.

---

## 🛠️ Tech Stack

- **Framework**: React 19 + Vite
- **Styling**: Tailwind CSS v4 + Custom Design Tokens (Milestone Yellow, River Slate, Alpine White)
- **Mapping**: Leaflet + React-Leaflet
- **Routing**: React Router DOM v7
- **Icons**: Lucide React
- **Typography**: IBM Plex Sans, IBM Plex Sans Condensed, IBM Plex Sans Devanagari

---

## ⚡ Getting Started

### Prerequisites
- Node.js (v18 or higher recommended)
- npm or yarn

### 1. Install Dependencies
```bash
npm install
```

### 2. Start the Development Server
```bash
npm run dev
```

Visit [http://localhost:5173](http://localhost:5173) in your browser.

### 3. Build for Production
```bash
npm run build
```

---

## 📁 Key Project Structure

```
Frontend/
├── src/
│   ├── api/             # API client and response adapters
│   ├── components/      # UI components (InteractiveMap, Layout, RainSimulationModal, etc.)
│   ├── data/            # Static highway segment registries & town coordinates
│   ├── pages/           # Application views (LiveMap, PlanTrip, Alerts, Report, Emergency, PastEvents)
│   ├── store/           # Global state (language context, simulation state)
│   ├── App.jsx          # Route configuration
│   └── main.jsx         # Application entry point
├── public/              # Static assets and icons
└── index.html           # HTML document template
```
