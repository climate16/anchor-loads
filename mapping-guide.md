# Anchor-Load Mapping Guide

How to find, verify and map **productive-use-of-energy (PUE) anchor loads** onto OpenStreetMap under `#AnchorLoads4EnergyAccess`.

Written for anyone joining the campaign — university cohorts, YouthMappers chapters, and independent mappers.

---

## 1. What counts as an anchor load

Facilities whose electricity demand is large and predictable enough to anchor a mini-grid's economics:

- **Agro-processing** — grain and maize mills, oil presses, sawmills, workshops
- **Cold chain** — cold stores, ice makers
- **Water** — powered pumping stations, boreholes
- **Institutions** — health centres, hospitals, schools
- **Commerce** — markets, including periodic market grounds
- **Connectivity and mobility** — telecom towers and masts, battery-swap and charging points

Households are not anchor loads. The point of this campaign is the facilities that make a grid viable.

---

## 2. Find → verify → correct or add

**Find.** Start from a public source (a schools or health-facility registry, a government dataset) or from local knowledge — someone who knows the area and can say what is actually there.

**Verify.** In [RapiD](https://rapideditor.org/), signed in with your OSM account, navigate to the location and check it against the imagery:
- Is it real, and is it in the right place?
- Is it already on OSM — and if so, correctly located and tagged?

**Correct or add.** Three outcomes, and two of them are the valuable ones:

| What you find | What you do | Value |
|---|---|---|
| On OSM, correct | Leave it | low |
| On OSM, **wrong** location or tag | **Fix it** | **high** |
| **Not on OSM** | **Add it** — draw the building footprint, or place a point, and apply the tag | **high** |

> Correcting and adding is the job — not confirming. A dot that is already right does not need you.

**In RapiD:** click *Point*, or *Area* to draw the building outline, place it, then type the facility in the search box ("mill", "clinic", "marketplace"). RapiD suggests the matching preset and applies the correct tag. Prefer drawing the **building area** when the footprint is clear; a point is fine otherwise.

### Never bulk-upload

A public list is a place to look, not a dataset to load. Automated or bulk uploads from a registry are an **import** under OSM's rules, require a separate community process, and get reverted if that process is skipped. Verify and place each feature by hand, and add only tags you can actually support from what you see or know.

---

## 3. The tag table

Applying the correct tag is what makes a feature searchable and correctly rendered. RapiD's preset search handles most of it; these are the targets. Rendering notes are against the standard [OSM Carto style](https://wiki.openstreetmap.org/wiki/OpenStreetMap_Carto/Symbols) — "generic marker" means it is stored correctly but shows a plain dot, so always add a clear `name`.

> **About `name=*`:** write the facility's real name — `name=Kabale Maize Mill`, or the operator if that is how it is known locally. The `*` is OSM notation for "the actual value goes here"; never type a literal `*`. A name is what turns an anonymous dot into something a planner can identify.

| Anchor load | OSM tag(s) | Renders as |
|---|---|---|
| **Telecom tower** (large) | `man_made=communications_tower` + `communication:mobile_phone=yes` | tower icon |
| **Telecom mast** (small BTS) | `man_made=mast` + `tower:type=communication` + `communication:mobile_phone=yes` | mast icon |
| **Large agro-processing mill** | `industrial=grinding_mill` + `name=*` | industrial/generic marker |
| **Small grain/maize mill** | `craft=grinding_mill` + `product=flour` | craft marker |
| **Oil press** | `man_made=works` + `product=oil` + `name=*` | generic marker |
| **Market** (incl. periodic) | `amenity=marketplace` | market icon |
| **Cold store / ice maker** | `building=warehouse` + `warehouse=cold_storage` + `name=*` | building outline |
| **Health centre / clinic** | `amenity=clinic` | clinic icon |
| **Hospital** | `amenity=hospital` | hospital icon |
| **School** | `amenity=school` | school icon |
| **Powered water pump / pumping station** | `man_made=pumping_station` + `name=*` | generic marker |
| **Borehole / well** | `man_made=water_well` | small icon |
| **Sawmill / workshop** | `craft=sawmill` (or `craft=*` for other trades) | craft marker |
| **E-mobility / battery-swap / charging** | `amenity=charging_station` | charging icon |

Unsure which tag fits? Add a clear `name` and `description`, apply the closest preset, and add a `fixme=*` note. Do not invent a tag you are not sure of.

---

## 4. Every edit needs two things

1. **The hashtag** — `#AnchorLoads4EnergyAccess` in the changeset comment. This is how the campaign's contributions are found; without it your work is invisible to the campaign, though still valuable to OSM.
2. **The correct tag** — from §3.

That is all. There is no separate reporting to file: OpenStreetMap is the record.

---

## 5. Local knowledge is the point

The facilities missing from every public registry — the market-day stalls, the small mill behind the church, the workshop no dataset lists — are the ones worth the most, and only people who know the area can find them.

If you are mapping in your own community, you already have what no remote mapper does. Map what you know, and add the `name` — that is where the deepest value in this campaign sits.

---

## Questions, or concerns about this activity

Contact marc@climate16.com, or leave a note on the [organised editing declaration](https://wiki.openstreetmap.org/wiki/Organised_Editing/Activities/Climate16_-_Anchor_Loads_for_Energy_Access) discussion page. We would rather hear from you early than after the fact.
