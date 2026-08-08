# Swedish Code of Statutes Open Data Repository — Svensk författningssamling (SFS)

This open-data repository provides machine-readable, canonical Markdown conversions of the **Swedish Code of Statutes** (*Svensk författningssamling — SFS*) sourced from the official Riksdagen Open Data API (`data.riksdagen.se`).

---

## Svenska / Swedish Overview

Detta öppna data-arkiv tillhandahåller maskinläsbara, kanoniska Markdown-konverteringar av **Svensk författningssamling (SFS)** hämtade från Riksdagens öppna data-API (`data.riksdagen.se`).

### Innehåll / Structure
- `sfs/<ÅR>/<NUMMER>.md`: En fil per SFS-författning med strukturerad YAML-frontmatter och omodifierad textkropp.
- `manifest.json`: Översikt över ögonblicksbild och antal dokument.
- `entries.json`: Spårning av SHA256-kontrollsummor per författning för exakt ändringshantering.
- `.last_sync.json`: Stämpel för automatisk daglig synkronisering.

---

## English Overview

### Repository Layout
- `sfs/<YEAR>/<NUMBER>.md`: One Markdown file per SFS statute containing structured YAML frontmatter allowlist and verbatim text body.
- `manifest.json`: Corpus snapshot metadata and counts.
- `entries.json`: SHA256 checksum registry for delta tracking.
- `.last_sync.json`: Stateful watermark for daily GitHub Actions refresh.

---

## Automated Daily Refresh / Automatisk uppdatering

An automated GitHub Action workflow (`.github/workflows/sfs-refresh.yml`) checks `data.riksdagen.se` daily at 03:30 UTC for updated or new SFS statutes, updates the repository files, and maintains stateful synchronization without data loss.

---

## Data Source & License / Datakälla & Licens

- **Source**: Riksdagens Öppna Data (`data.riksdagen.se`).
- **Legal Status**: Swedish public statutes are public domain (*Offentlighets- och sekretesslagen / Tryckfrihetsförordningen*).
