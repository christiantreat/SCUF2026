# SCUF 2026 — Point-of-Care Ocular Ultrasound Simulator

A single-file, offline-capable HTML simulator for teaching ocular point-of-care ultrasound (POCUS). Built for conference workshops and self-directed learning. Runs from a USB stick on any laptop — no install, no login, no internet required.

## How to Use

1. Open `ocular-pocus-simulator.html` in any modern browser
2. **Drag left/right** to sweep the probe across the globe
3. **Drag up/down** to adjust gain
4. **Spacebar** or **Eye Move** button to trigger patient eye movement (for washing machine sign)
5. Toggle between 4 modes: **Normal**, **VH**, **RD Mac-On**, **RD Mac-Off**
6. Toggle **Labels** to show/hide anatomy annotations

## Simulator Modes

### Normal Globe

- High-frequency linear probe (10 MHz), ophthalmologic/small-parts preset (MI < 0.23)
- Tegaderm over closed lid, generous gel, stabilize hand on brow
- Depth 4-5 cm. Vitreous is anechoic — no internal echoes at appropriate gain
- Posterior wall: retina + choroid + sclera (RCS complex) appear as single bright line
- ONSD measured 3 mm behind globe: normal < 5 mm (96% sensitive for elevated ICP)
- Contraindicated if globe rupture suspected

### Vitreous Hemorrhage (VH)

- **Washing machine sign** — debris swirls with PATIENT EYE MOVEMENT, not probe sweep
- Sensitivity improves with gain: 71% at low gain, 88% at high gain (Wenger et al. 2023) — always screen at high gain
- Free-floating particles, NOT tethered to optic disc (key differentiator vs RD)
- 67% of fundus-obscuring VH have an associated retinal tear (POCUS Atlas)
- Blood settles with gravity when eye is still — use kinetic exam to trigger washing machine sign
- Compare to PVD: both untethered, but VH = diffuse particles vs PVD = thin membrane

### Retinal Detachment — Mac-On (Surgical Emergency)

- Macula STILL ATTACHED — emergent repair within hours to preserve central vision
- Detachment on nasal side of disc — does NOT extend past macula (3 mm temporal to disc)
- More subtle presentation: patient may still have relatively good central vision
- Higher risk of missed diagnosis — use ultrasound to confirm suspected RD
- Thick hyperechoic membrane tethered at optic disc, curving along globe wall (gain-independent)
- Limited aftermovement on kinetic exam — stiffer than VH, stays anchored at disc

### Retinal Detachment — Mac-Off (Urgent, 24-72h)

- Macula DETACHED — central vision already compromised. Urgent repair within 24-72 hours
- Membrane on temporal side of disc — extends past macula position
- Tethered at optic disc, curving along globe wall toward ora serrata anteriorly
- Gain-independent: 97-100% sensitivity at ALL gain levels (Wenger et al. 2023)
- Chronic RD: evolves V to Y/T to funnel shape, membrane thickens, aftermovement decreases
- Always screen at high gain to check for concurrent vitreous hemorrhage

## Sonoanatomy

The simulator renders anatomically proportioned structures based on published measurements:

- **Globe**: 24 mm axial length (12 mm radius)
- **Anterior chamber**: ~2.2 mm depth
- **Iris**: with central pupil opening
- **Lens**: biconvex, ~4.5 mm thick x 9 mm diameter, anterior and posterior capsules
- **Vitreous**: anechoic at appropriate gain
- **Posterior wall**: retina/choroid/sclera (RCS complex) as single echogenic line, interrupted at the optic disc (hypoechoic gap)
- **Optic nerve**: with sheath, ONSD measurement line at 3 mm behind globe
- **Macula**: 3 mm temporal to optic disc margin (~4 mm center-to-center)
- **Extraocular muscles**: medial and lateral rectus

## Machine Settings Displayed

- MI 0.23, TIs 0.4 (ophthalmic safety limits)
- Gain (adjustable 10-95 dB)
- 10 MHz frequency
- DR 60 (dynamic range)
- Focus indicator triangle
- TGC (time-gain compensation) bars
- Depth markers (1-4 cm)

## Key Teaching Points

| Feature | VH | RD |
|---|---|---|
| Tethered to disc | No | Yes |
| Gain-dependent | Yes (71-88%) | No (97-100%) |
| Aftermovement | Swirling (washing machine) | Limited, stiff |
| Triggered by | Patient eye movement | Always visible |
| Gravity settling | Yes | No |

## FOAME References

1. **The POCUS Atlas** — Ocular section. RD sensitivity 97-100%, specificity 83-100%. [thepocusatlas.com/ocular](https://www.thepocusatlas.com/ocular)
2. **ALiEM** — Ocular Ultrasound: RD vs PVD differentiation, probe technique, kinetic exam. [aliem.com/ocular-ultrasound](https://www.aliem.com/ocular-ultrasound-retinal-detachment-posterior-vitreous-detachment/)
3. **POCUS 101** — Step-by-step guide: washing machine sign, gain optimization, technique pearls. [pocus101.com/ocular-ultrasound](https://www.pocus101.com/ocular-ultrasound-made-easy-step-by-step-guide/)
4. **JETem** — Mac-off RD on bedside US. Mac-on vs mac-off urgency, tethering anatomy. [jetem.org/mac-off-rd](https://jetem.org/mac-off-rd/)
5. **JETem** — Bedside US of RD in a 19-year-old. Sensitivity/specificity data. [jetem.org/retinaldetachment_ultrasound](https://jetem.org/retinaldetachment_ultrasound/)
6. **ACEP Sonoguide** — Ocular emergencies, kinetic assessment, aftermovement evaluation. [acep.org/sonoguide](https://www.acep.org/sonoguide/advanced/ocular-emergencies)
7. **StatPearls** — Point-of-care ocular US. Probe settings, safety (MI < 0.23), contraindications. [ncbi.nlm.nih.gov/books/NBK459120](https://www.ncbi.nlm.nih.gov/books/NBK459120/)
8. **Wenger et al. 2023** — Gain optimization (Western J Emerg Med). VH: 71% low to 88% high. RD: 97-98% all gains. [PMC10284517](https://pmc.ncbi.nlm.nih.gov/articles/PMC10284517/)
9. **LITFL** — Ocular US library, clinical cases, and the Ocular Ultrasound Challenge. [litfl.com/ocular-ultrasound](https://litfl.com/ultrasound-library/ocular-ultrasound/)
10. **EMOttawa** — ONSD < 5 mm, optic disc elevation, technique pearls. [emottawablog.com](https://emottawablog.com/2022/08/ocular-pocus-keep-your-prize-on-the-eyes/)
11. **Core EM** — Ocular US overview, retinal vs vitreous detachment, ONSD, CRAO. [coreem.net/core/ocular-ultrasound](https://coreem.net/core/ocular-ultrasound/)

## Conference Projects

| Project | Description |
|---|---|
| [SonoGames](https://github.com/christiantreat/sonogames) | Ultrasound gamification for education |
| [SonoWolf](https://github.com/christiantreat/sonowolf) | Social deduction game for US interpretation |
| [UltraClean](https://github.com/christiantreat/ultraclean) | Ultrasound image optimization tools |
| [Zine](https://github.com/christiantreat/zine) | Visual learning zines for point-of-care ultrasound |

## For Educational Use Only

This simulator is a teaching aid for understanding ocular ultrasound concepts. It is not a diagnostic tool and should not be used for clinical decision-making.
