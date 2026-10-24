# FLOODPULSE — Flood Intelligence Website

A responsive front-end prototype for **Team Astrocode**, based on the FLOODPULSE presentation for Nakshatra Aerospace Hackathon 2026 (Software Track, PS-01).

## Included
- Mission overview dashboard with sample indicators
- Satellite scene file selection UI
- NDWI / MNDWI selection and planned Sentinel-1 SAR option
- Clickable illustrative flood layer
- Four-stage Acquire → Detect → Assess → Report workflow
- Settlement watchlist
- Exportable demo impact report in CSV format
- Responsive layout for desktop, tablet, and mobile

## Run locally
1. Extract the ZIP.
2. Open the `FLOODPULSE_Website` folder in VS Code.
3. Open `index.html` in a browser, or use the VS Code **Live Server** extension and click **Go Live**.
4. No package installation is needed for this front-end demo.

## Important technical note
This package is a front-end demonstration. The progress bar simulates a workflow; it does **not** process uploaded imagery or calculate real NDWI, flood extent, or settlement exposure. The map is a schematic illustration and all dashboard numbers and settlement records are sample data.

To turn this into a validated geospatial application, connect a backend that can:
- Read georeferenced imagery (GeoTIFF / Sentinel-2 products)
- Apply cloud and quality masking
- Compute NDWI/MNDWI and temporal change masks
- Reproject and clip scenes to a defined AOI
- Read settlement boundaries from GeoJSON / a GIS source
- Intersect flood polygons with settlement geometries
- Export real GeoJSON and a generated PDF/CSV report
- Track provenance, acquisition dates, thresholds, and validation results

The presentation calls out cloud obstruction, threshold sensitivity, and settlement boundary gaps as risks. Validate outputs against ground truth before operational use. Do not present prototype values as live or verified emergency intelligence.

## Project structure
```text
FLOODPULSE_Website/
├── index.html
├── styles.css
├── app.js
├── README.md
└── assets/
    └── (reserved for project logo / validated imagery)
```
