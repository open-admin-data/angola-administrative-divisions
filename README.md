# Angola Administrative Divisions / Angola



## Overview

| Item | Details |
|------|---------|
| Province | 18 |
| Municipality | 161 |
| Commune | 539 |
| Coordinates | ✅ Included (all levels) |
| Formats | JSON, NDJSON, CSV |
| License | CC-BY-4.0 |
| Last Updated | 2026-09-08 |
| Website | [openadmindata.org/ao](https://openadmindata.org/ao/) |
| API | [openadmindata.org/api/ao](https://openadmindata.org/api/ao/) |
| Flag | [PNG](https://onlygames.me/flags-png/ao/) · [CDN](https://www.freeflags.org/cdn/) · [CSS](https://www.freeflags.org/css/) · [Collections](https://www.freeflags.org/collections/) |
| National Anthem | [🎵 Listen & Download Angola National Anthem MP3](https://onlygames.me/national-anthems/ao/) |
| Statistics | [GDP](https://nationdata.org/gdp/country/ago) · [Population](https://nationdata.org/population/country/ago) — via [NationData.org](https://nationdata.org) |

## Browse by Province

| # | Province | Municipalitys | Communes | Link |
|---|----|----|----|------|
| 1 | Bengo | 6 | 23 | [Browse](divisions/bengo-ao01/) |
| 2 | Benguela | 10 | 35 | [Browse](divisions/benguela-ao02/) |
| 3 | Bié | 9 | 36 | [Browse](divisions/bi-ao03/) |
| 4 | Cabinda | 4 | 12 | [Browse](divisions/cabinda-ao04/) |
| 5 | Cuando Cubango | 9 | 27 | [Browse](divisions/cuando-cubango-ao05/) |
| 6 | Cuanza Norte | 10 | 31 | [Browse](divisions/cuanza-norte-ao06/) |
| 7 | Cuanza Sul | 12 | 36 | [Browse](divisions/cuanza-sul-ao07/) |
| 8 | Cunene | 6 | 20 | [Browse](divisions/cunene-ao08/) |
| 9 | Huambo | 11 | 37 | [Browse](divisions/huambo-ao10/) |
| 10 | Huíla | 14 | 38 | [Browse](divisions/hula-ao09/) |
| 11 | Luanda | 7 | 39 | [Browse](divisions/luanda-ao11/) |
| 12 | Lunda Norte | 9 | 25 | [Browse](divisions/lunda-norte-ao12/) |
| 13 | Lunda Sul | 4 | 16 | [Browse](divisions/lunda-sul-ao13/) |
| 14 | Malanje | 14 | 51 | [Browse](divisions/malanje-ao14/) |
| 15 | Moxico | 9 | 31 | [Browse](divisions/moxico-ao15/) |
| 16 | Namibe | 5 | 14 | [Browse](divisions/namibe-ao16/) |
| 17 | Uíge | 16 | 47 | [Browse](divisions/uge-ao17/) |
| 18 | Zaire | 6 | 21 | [Browse](divisions/zaire-ao18/) |

## Data Files

| File | Format | Description |
|------|--------|-------------|
| [all-province.json](data/all-province.json) | JSON | All 18 province records |
| [all-municipality.json](data/all-municipality.json) | JSON | All 161 municipality records |
| [all-commune.json](data/all-commune.json) | JSON | All 539 commune records |
| [all-flat.json](data/all-flat.json) | JSON | Levels 1-2 flat array |
| [all-flat.ndjson](data/all-flat.ndjson) | NDJSON | Streaming format |
| [all-flat.csv](data/all-flat.csv) | CSV | Spreadsheet format |
| [hierarchy.json](data/hierarchy.json) | JSON | Nested tree |
| [schema.json](data/schema.json) | JSON Schema | Data schema |

## Quick Start

### Python

```python
import json

with open("data/all-province.json", "r", encoding="utf-8") as f:
    data = json.load(f)

for r in data:
    print(f"{r['name']['local']} ({r['name']['en']}) — {r['children_count']['municipality']} municipalitys")
```

### JavaScript

```javascript
import { readFileSync } from "fs";

const data = JSON.parse(readFileSync("data/all-province.json", "utf-8"));
console.log(`Total: ${data.length} provinces`);
```

## Schema

| Field | Type | Description |
|-------|------|-------------|
| `id` | string | Unique identifier |
| `level` | integer | 1=province, 2=municipality, 3=commune |
| `level_name` | object | Level label (local + English) |
| `name.local` | string | Name in local script |
| `name.en` | string | English name |
| `name.slug` | string | URL-safe slug |
| `parent` | object/null | Parent division reference |
| `ancestors` | array | Full ancestor chain |
| `children_count` | object | Count of children per level |
| `zip_codes` | array | Postal codes (where available) |
| `geo.lat` | string | Latitude (WGS84) |
| `geo.lon` | string | Longitude (WGS84) |

Full schema: [data/schema.json](data/schema.json)

## Hierarchy Browse

```
divisions/{province-slug}/
divisions/{province-slug}/{municipality-slug}/
```

Communes are listed inline in each municipality's README.

## AI Integration

- [llms.txt](docs/llms.txt) — Quick reference for AI agents
- [llms-full.txt](docs/llms-full.txt) — Summary with per-province links
- [Per-province data](docs/llms-full/) — Full data by province

## Citation

```
Angola Administrative Divisions Dataset (CC-BY-4.0)
URL: https://github.com/open-admin-data/angola-administrative-divisions
```

See [CITATION.cff](CITATION.cff) for machine-readable citation.

## License

- **Data**: [CC-BY-4.0](LICENSE)

## Related

- [Open Admin Data](https://openadmindata.org) — Browse, search and explore administrative divisions for every country
- [open-admin-data](https://github.com/open-admin-data) — GitHub organization with all country repos
- [ListBase](https://www.listbase.org) — Structured reference data for every country
- [FreeFlags.org](https://www.freeflags.org) — Free flag images for every country
- [Flag CDN](https://www.freeflags.org/cdn/) — Hotlink flag images directly
- [Flag CSS](https://www.freeflags.org/css/) — CSS flag sprites for web projects
- [Flag Collections](https://www.freeflags.org/collections/) — Curated flag image packs
