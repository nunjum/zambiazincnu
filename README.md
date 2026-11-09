# Project Trace: Zinc Asymmetry Framework
### Tracing zinc and co-located lead from Kabwe, Zambia to its end uses (Assignment Iteration 2)

A single-file static site that traces zinc, and the lead found alongside it, from Kabwe, Zambia to its end uses, and shows who earns what and who absorbs the harm.

**Argument:** demand for transition metals rewards re-extraction of toxic waste while children pay the health cost.

**Scope note:** Kabwe's poisoning is mainly **lead**. Zinc is the co-product that makes reprocessing the waste piles profitable. Health figures on the site are about lead; price and trade figures are about zinc.

## Evidence rules

Every figure comes from a fixed data pack. Anything not in the pack is labelled **UNVERIFIED** on the page.

| Tag | Meaning |
|---|---|
| `[SAYARI]` | Sayari trade/ownership data |
| `[WEB]` | Public source (URL in the source log on the Methodology tab) |
| `ALLEGED` | Claimed, disputed or unanswered by the company named |
| `UNVERIFIED` | Not in the data pack |

---

## Repository layout

* `index.html`: the whole site. Semantic HTML5, Tailwind via CDN, six tabbed views, a few lines of vanilla JS.
* `README.md`: this file.

Open `index.html` in a browser; no build step. (Tailwind and the page need network access for the CDN script.)

---

## The six views

### 1. Timeline (four epochs)
1. **c. 1902 – 1994, mining.** Lead-zinc mine operated from roughly 1902, 1904 or 1906 (sources differ) until 1994; ZCCM owned it at closure. Anglo American class action (about 140,000 women and children) alleges its 1925–1974 operations contributed to the pollution; Anglo denies causing current conditions (**alleged / disputed**).
2. **1994 – 2024, legacy.** About 6.4 million tonnes of uncovered waste remain. World Bank ZMERIP: US$65.6M IDA credit (a loan), approved Dec 2016, funded testing, treatment and hotspot remediation but did not remove the source. End date unverified.
3. **2025, re-extraction.** HRW documents waste processing by South African, Chinese and local firms; Zambia designates Kabwe zinc and lead "critical minerals"; miners allege sales to Datong Industries, Chengde Mining and Superdeal Investments (**alleged**, companies did not respond); Zambia permits Hua Yu Sheng to take control of most of the lead waste for zinc extraction (late 2025; ownership unverified, no Sayari record); Anglo appeal hearing 5 Nov 2025.
4. **2026, AU complaint.** IHRDA files an African Union child-rights complaint against Zambia on 16 Apr 2026; the committee was scheduled to consider it on 20 Oct 2026 (outcome unverified).

### 2. End products
Bar chart of global zinc use in 2024 (ILZSG via Natural Resources Canada): galvanizing 60%, zinc alloys 15%, compounds 11%, brass and bronze 9%, semi-manufactures 4%, other 1%. HRW names wind turbines, solar and hydro as uses. An **open question** card states that no documented link was found between Kabwe zinc and high-voltage semiconductors, fusion-reactor coils or Helion Energy.

### 3. Financial ledger
Five nodes (scavenging, aggregation, refining, component fab, deployment) by beneficiary, figure, source tag and liability absorbed. Only cells the data pack supports are filled; the rest read "UNVERIFIED / not found". Also shows a zinc price benchmark (about US$3,670–3,900/t in Sept–Oct 2026; Nov 2025 LME cash average US$3,186.65/t), the ZMERIP loan, and the estimated social cost of lead pollution (US$224–593M, secondary source: Yamada et al. as cited by HRW). The DCPL policy proposal sits here, labelled as a proposal, not evidence.

### 4. Biomedical harm
More than 95% of children near the mine have elevated blood lead and about half need urgent treatment (2018 study cited by HRW); up to about 200,000 people exposed; soil lead up to 60,000 mg/kg against a 200 mg/kg hazard level; many children above 45 µg/dL; reported learning disabilities, behavioural problems, organ damage, miscarriages and stillbirths; children as young as 7 doing waste-pile work. "Children absorb 5× adults" and maternal bone-lead mobilisation are labelled UNVERIFIED.

### 5. Trade map
Sayari search (zinc, departure country Zambia): 488 supplier records; buyer-country record counts; exporters of zinc ores and concentrates (HS 2608) by shipment records; Sable Zinc Kabwe Ltd; buyers of Zambian zinc ore. **These flows are largely transit via Tanzania and include DRC-origin concentrate, so they cannot be attributed to Kabwe waste.** Counts are record counts, not tonnage or value. The 102 of 488 ILAB child-labour flags are country/product-level risk indicators, not evidence of child labour at those firms.

### 6. Methodology
Source log (URL, date, tag), caveats, a "Claims I could not verify" list, and the backlog.

---

## Policy proposal: Decentralized Cryptographic Provenance Ledger (DCPL)

The authors' proposal, not evidence, and it has not been piloted.
1. **Automated hash verification:** every raw payload crossing a border generates a distributed token linked to a verified local Environmental Impact Assessment (EIA).
2. **Market metric reversal:** unverified minerals are kept out of international exchange pricing tiers.
3. **Smart-contract supply locks:** purchasing pipelines require traceability from extraction origin to deployment.

---

## Removed from earlier drafts (unsourced)

* "$1–2 per day" child wage. The only pay data is one adult scavenger's 2016 account (50 kwacha, about US$5, per 25 kg sack).
* "+80% global zinc demand by 2050."
* CHIPS Act subsidies and "trillions in net-zero market valuations."
* Galvanizing "for maritime wind turbine assemblies."
* Kabwe zinc in high-voltage semiconductors, fusion coils and Helion (now an open question).
* Zambia "overriding its own environmental law."
* "Blood lead above 45 µg/dL causes permanent cognitive and memory degradation," and "5× absorption" stated as fact.
* The HRW report title (not in the data pack; cited by URL).

## Backlog

* Kabwe-origin export data
* Refiner margins
* Scavenger pay with a 2025–2026 source
* Hua Yu Sheng ownership via Chinese company registry
* Verify the semiconductor/fusion link, or drop it

---

## Sources

Full log with URLs, dates and tags is on the Methodology tab of the site. Principal sources: HRW (5 Mar 2025 article; 20 Oct 2026 op-ed), BHRRC (5 Nov 2025), World Bank press release (16 Dec 2016), Global Press Journal (23 Oct 2016), Trading Economics, USGS MIS (Nov 2025), ILZSG via Natural Resources Canada, and Sayari Graph.

---

## Git

```bash
cd /Users/nafisaunjum/New-Updated-SA/ZambiaZinc
git status
git add index.html README.md
git commit -m "docs: rebuild site on sourced data pack; label unverified claims; add trade map and source log"
git push origin main
```
