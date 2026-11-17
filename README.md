# CCNM v2 – Care Unit Nutrition Monitoring

A single-page web app for monitoring and evaluating patient progress with nutrition care, medication and total parenteral nutrition (TPN) in critical care and renal units, now with an **NBU (neonatal) feeds monitoring module**.

> **Decision-support aid only. Not for diagnosis.** Clinical decisions rest with the treating team and local protocols.

## Modules
- **Dashboard**: per-patient summary and alerts
- **Nutrition care**: energy/protein target vs delivered, fluid balance, renal markers (K⁺, Na⁺, PO₄, urea, creatinine)
- **Medication**: active/stopped list with nutrition relevance notes
- **TPN**: dextrose, amino acids, lipid; calculated kcal, kcal/kg and GIR
- **NBU feeds** (new): feed prescription, feed log (offered/taken, aspirates, vomiting, distension), daily weights with growth chart, ml/kg/day (enteral + TPN), kcal/kg/day, weight velocity, and configurable alerts
- **Settings & data**: alert thresholds, milk kcal values, JSON export/import
## Run it
https://naire-arch.github.io/ccnm2-0/.

## Data and privacy
All data is stored in the browser's `localStorage` on that device only. Nothing is sent anywhere. Use patient aliases unless your governance permits identifiers, and export JSON backups regularly. Clearing browser data erases records.

## NBU calculations
- ml/kg/day = (volume taken, plus TPN volume) ÷ weight (kg)
- Energy = milk volume × kcal/100 ml (editable in Settings) + TPN (dextrose 3.4, amino acids 4, lipid 10 kcal/g)
- Weight velocity (g/kg/day) uses the average weight over the no-gain window
- Alert thresholds (weight loss %, no-gain days, low intake %, large aspirate %) are defaults and **must be set to local protocol**


