# N64 Board Revision Reference

A comprehensive record of Nintendo 64 motherboard revisions across all regions, documenting component profiles, production evidence, and known variances. Values, markings, and identifications are grounded in primary source material; confidence level is stated explicitly where evidence is incomplete.

---

## Contents

* [§1 Introduction](#1-introduction)
    * [§1.1 Scope](#11-scope)
    * [§1.2 Methodology](#12-methodology)
    * [§1.3 Confidence Hierarchy](#13-confidence-hierarchy)
    * [§1.4 Conventions](#14-conventions)
* [§2 Revision Overview](#2-revision-overview)
    * [§2.1 NTSC Revisions](#21-ntsc-revisions)
    * [§2.2 PAL Revisions](#22-pal-revisions)
    * [§2.3 PAL-M Revisions](#23-pal-m-revisions)
* [§3 Component Profiles](#3-component-profiles)
    * [§3.1 CPU (VR4300 / CPU-NUS)](#31-cpu-vr4300--cpu-nus)
    * [§3.2 RCP (Reality Co-Processor / RCP-NUS)](#32-rcp-reality-co-processor--rcp-nus)
    * [§3.3 Clock Generation (U7 / U15)](#33-clock-generation-u7--u15)
    * [§3.4 Video Output Path](#34-video-output-path)
    * [§3.5 Audio DAC](#35-audio-dac)
    * [§3.6 PIF-NUS](#36-pif-nus)
    * [§3.7 RDRAM](#37-rdram)
    * [§3.8 Support Logic (U8)](#38-support-logic-u8)
    * [§3.9 Voltage Regulation](#39-voltage-regulation)
* [§4 Board Revision Entries](#4-board-revision-entries)
    * [§4.1 NTSC](#41-ntsc)
        * [NUS-CPU-01](#nus-cpu-01)
        * [NUS-CPU-02](#nus-cpu-02)
        * [NUS-CPU-03](#nus-cpu-03)
        * [NUS-CPU-04](#nus-cpu-04)
        * [NUS-CPU-05](#nus-cpu-05)
        * [NUS-CPU-05-1](#nus-cpu-05-1)
        * [NUS-CPU-06](#nus-cpu-06)
        * [NUS-CPU-07](#nus-cpu-07)
        * [NUS-CPU-08](#nus-cpu-08)
        * [NUS-CPU-08-1](#nus-cpu-08-1)
        * [NUS-CPU-09](#nus-cpu-09)
        * [NUS-CPU-09-1](#nus-cpu-09-1)
    * [§4.2 PAL](#42-pal)
        * [NUS-CPU(R)-01](#nus-cpur-01)
        * [NUS-CPU(P)-01](#nus-cpup-01)
        * [NUS-CPU(P)-02](#nus-cpup-02)
        * [NUS-CPU(P)-03](#nus-cpup-03)
        * [NUS-CPU(P)-03-1](#nus-cpup-03-1)
    * [§4.3 PAL-M](#43-pal-m)
        * [NUS-CPU(M)-01](#nus-cpum-01)
        * [NUS-CPU(M)-02](#nus-cpum-02)
        * [NUS-CPU(M)-03](#nus-cpum-03)
        * [NUS-CPU(M)-04](#nus-cpum-04)
        * [NUS-CPU(M)-05](#nus-cpum-05)
        * [NUS-CPU(M)-05-1](#nus-cpum-05-1)
    * [§4.4 Engineering Samples](#44-engineering-samples)
        * [NUS-CPU-E7I](#nus-cpu-e7i)
* [§5 Production Evidence](#5-production-evidence)
    * [§5.1 PCB Date Codes](#51-pcb-date-codes)
    * [§5.2 IC Date Codes](#52-ic-date-codes)
    * [§5.3 Crystal Corpus](#53-crystal-corpus)
    * [§5.4 Component Transition Brackets](#54-component-transition-brackets)
* [§6 Sources](#6-sources)
    * [§6.1 Figures](#61-figures)
    * [§6.2 References](#62-references)
    * [§6.3 Acknowledgements](#63-acknowledgements)
* [Glossary](#glossary)

---

## 1. Introduction

[TODO]

### 1.1 Scope

[TODO - iQue *may* be outside scope. We intend to at least acknowledge early iterations / prototype hardware.]

### 1.2 Methodology

[TODO -- Gold example approach. Every entry anchored to at least one exhaustively documented board. Variances noted explicitly against the gold. Front and back of board. Source attribution per marking.]

### 1.3 Confidence Hierarchy

[TODO]

### 1.4 Conventions

[TODO]

---

## 2. Revision Overview

Summary tables. One row per revision. Abridged; full profiles in §4.

### 2.1 NTSC Revisions

Revision     | PCB Date (range) | CPU-NUS     | Clock Gen                         | Video Path            | RDRAM            | CPU+RCP Heatsinks | Notes
:----------- | :--------------- | :---------- | :-------------------------------- | :-------------------- | :--------------- | :---------------- | :------------------------------------------------------------------------------
NUS-CPU-01   |                  | CPU-NUS     | 2x MX8330MC                       | VDC-NUS + ENC-NUS     | 2x RDRAM18-NUS A | Discrete          | Rare, posited to be NUS-001(JPN)-only
NUS-CPU-02   |                  | CPU-NUS     | 2x MX8330MC                       | VDC-NUS + ENC-NUS     | 2x RDRAM18-NUS A | Discrete          |
NUS-CPU-03   |                  | CPU-NUS (A) | 2x MX8330MC                       | VDC-NUS (A) + ENC-NUS | 2x RDRAM18-NUS A | Discrete          | First appearance of CPU-NUS A (mid-run) and VDC-NUS A (mid-run)
NUS-CPU-04   |                  | CPU-NUS A   | 2x MX8330MC                       | VDC-NUS A + ENC-NUS   | 2x RDRAM18-NUS B | Discrete          | First appearance of RDRAM18-NUS B
NUS-CPU-05   |                  | CPU-NUS A   | MX8330MC + MX9911MC               | AVDC-NUS (MAV-NUS)    | 2x RDRAM18-NUS B | Discrete          | Only appearance of AVDC-NUS; first appearance of MAV-NUS (mid-run) and MX9911MC
NUS-CPU-05-1 |                  | CPU-NUS A   | MX8330MC + MX9911MC (2x MX9911MC) | MAV-NUS               | 2x RDRAM18-NUS B | Discrete          | First appearance of dual MX9911MC; overlaps 05
NUS-CPU-06   |                  | CPU-NUS A   | MX8330MC + MX9911MC (?)           | MAV-NUS               | RDRAM36-NUS      | Discrete          | First appearance of RDRAM36-NUS; very rare; overlaps 05
NUS-CPU-07   |                  | CPU-NUS A   | MX8330MC + MX9911MC (?)           | MAV-NUS               | RDRAM36-NUS      | Discrete          | Very rare; overlaps 05
NUS-CPU-08   |                  | CPU-NUS A   | MX8350                            | MAV-NUS               | RDRAM36-NUS      | Discrete          | First appearance of MX8350
NUS-CPU-08-1 |                  | CPU-NUS A   | MX8350                            | MAV-NUS               | RDRAM36-NUS      | Discrete          |
NUS-CPU-09   |                  | CPU-NUS A   | MX8350                            | MAV-NUS               | RDRAM36-NUS      | Integrated        | First appearance of integrated CPU/RCP heatsinks
NUS-CPU-09-1 |                  | CPU-NUS A   | MX8350                            | MAV-NUS               | RDRAM36-NUS      | Integrated        |


### 2.2 PAL Revisions

Revision        | PCB Date (range) | CPU-NUS       | Clock Gen                         | Video Path          | RDRAM            | CPU+RCP Heatsinks | Notes
:-------------- | :--------------- | :------------ | :-------------------------------- | :------------------ | :--------------- | :---------------- | :--------------------------------------------------------------
NUS-CPU(P)-01   |                  | [unconfirmed] | 2x MX8330MC (MX8330MC + MX9911MC) | DENC-NUS            | 2x RDRAM18-NUS A | Discrete          | Only appearance of DENC-NUS
NUS-CPU(P)-02   |                  | CPU-NUS A     | [unconfirmed]                     | MAV-NUS             | [unconfirmed]    | Discrete          |
NUS-CPU(P)-03   |                  | CPU-NUS A     | [unknown]                         | MAV-NUS             | [unknown]        | [unknown]         | Entirely undocumented, provenance unconfirmed; likely very rare
NUS-CPU(P)-03-1 |                  | CPU-NUS A     | MX8350                            | MAV-NUS             | RDRAM36-NUS      | Integrated        | Likely (very) rare, posited to be AUS-only


Revision        | PCB Date (range) | CPU-NUS       | Clock Gen                         | Video Path          | RDRAM            | CPU+RCP Heatsinks | Notes
:-------------- | :--------------- | :------------ | :-------------------------------- | :------------------ | :--------------- | :---------------- | :--------------------------------------------------------------
NUS-CPU(R)-01   |                  | [unconfirmed] | 2x MX8330MC                       | VDC-NUS A + S-RGB A | 2x RDRAM18-NUS A | Discrete          | Rare; NUS-001(FRA) only


### 2.3 PAL-M Revisions

Revision        | PCB Date (range) | CPU-NUS       | Clock Gen     | Video Path              | RDRAM            | CPU+RCP Heatsinks | Notes
:-------------- | :--------------- | :------------ | :------------ | :---------------------- | :--------------- | :---------------- | :---------------------------------
NUS-CPU(M)-01   |                  | [unconfirmed] | 2x MX8330MC   | VDC-NUS (?) + ENC-NUS   | 2x RDRAM18-NUS A | Discrete          |
NUS-CPU(M)-02   |                  | [unconfirmed] | [unconfirmed] | VDC-NUS A (?) + ENC-NUS | [unconfirmed]    | Discrete          |
NUS-CPU(M)-03   |                  | CPU-NUS A     | [unconfirmed] | MAV-NUS?                | [unconfirmed]    | Discrete          |
NUS-CPU(M)-04   |                  | [unknown]     | [unknown]     | [unknown]               | MAV-NUS          | [unknown]         | Entirely undocumented; likely (very) rare
NUS-CPU(M)-05   |                  | [unknown]     | [unknown]     | [unknown]               | MAV-NUS          | [unknown]         | Entirely undocumented; likely (very) rare
NUS-CPU(M)-05-1 |                  | CPU-NUS A     | MX8350        | MAV-NUS                 | RDRAM36-NUS      | Integrated        |


---

## 3. Component Profiles

Each section traces a single component or subsystem across the full production run.

### 3.1 CPU (VR4300 / CPU-NUS)

[TODO -- CPU-NUS vs CPU-NUS A transition. PRId values. mulmul / SRA bug scope. Mask work notation. Earliest/latest known datecodes per variant.]

### 3.2 RCP (Reality Co-Processor / RCP-NUS)

[TODO -- Known variants if any. Mask work. Datecodes across corpus.]

### 3.3 Clock Generation (U7 / U15)

[TODO -- MX8330MC, MX9911MC, MX8350 progression. Visual identification. FSEL logic. Production brackets. Mixed-pair configurations. U15 identity per revision.]

### 3.4 Video Output Path

[TODO -- Full chip family: VDC-NUS, VDC-NUS A, ENC-NUS, DENC-NUS, S-RGB A, AVDC-NUS, MAV-NUS. Two-chip vs single-chip path. Audio DAC integration point. AVDC/MAV shared pinout. Multi-vendor MAV-NUS (BU9906F, RS5C382). Disambiguation rules.]

### 3.5 Audio DAC

[TODO -- BU9480F as standalone chip. Integration into AVDC-NUS / MAV-NUS. Revisions where BU9480F is absent. DENC-NUS does not integrate audio.]

### 3.6 PIF-NUS

[TODO -- Regional variants: PIF-NUS, PIF(M)-NUS, PIF(P)-NUS. Date code format. Known markings across corpus.]

### 3.7 RDRAM

[TODO -- 2x RDRAM18-NUS A to 1x RDRAM36-NUS transition. Transition point (NUS-CPU-06 or later). Datecodes across corpus.]

### 3.8 Support Logic (U8)

[TODO -- TI SN74LVC125, TI LV125A, Toshiba TC74LCX125, ST 74LCX125, unknown VC125A. Known revisions per variant. Gaps.]

### 3.9 Voltage Regulation

[TODO -- Sharp PQ7VZ5 and variants. Mitsumi PST9128. Known markings. Revisions.]

---

## 4. Board Revision Entries

Each entry follows a consistent structure:

* **Gold example(s)**: The board(s) from which the entry profile is primarily derived. Source credited.
* **Revision marking**: Board marking as observed, verbatim.
* **PCB date code**: As observed; decoded where possible.
* **Component profile**: Every identifiable IC and marking, front and back.
* **Known variances**: Departures from the gold profile observed in other examples of the same revision.
* **Production notes**: Overlap with adjacent revisions, transition observations, open questions.
* **Confidence**: Entry-level confidence per §1.3.

---

### 4.1 NTSC

#### NUS-CPU-01

*Gold candidate: Prominos_01*

[TODO]

---

#### NUS-CPU-02

*Gold candidate: Prominos_02*

[TODO]

---

#### NUS-CPU-03

*Gold candidate: Prominos_03*

[TODO]

---

#### NUS-CPU-04

*Gold candidate: Prominos_04*

[TODO]

---

#### NUS-CPU-05

*Gold candidate: Prominos_05*

[TODO]

---

#### NUS-CPU-05-1

*Gold candidate: Prominos_05-1*

[TODO]

---

#### NUS-CPU-06

*Gold candidate: pending (grav)*

[TODO -- Extremely rare. One known image of reasonable quality (DragonsHoardLabs). Awaiting higher-resolution example.]

---

#### NUS-CPU-07

*Gold candidate: pending (grav)*

[TODO -- Extremely rare. U15 = MX8330MC confirmed (ChipWorks). U7 identity unconfirmed photographically.]

---

#### NUS-CPU-08

*Gold candidate: Prominos_08*

[TODO]

---

#### NUS-CPU-08-1

[TODO]

---

#### NUS-CPU-09

[TODO]

---

#### NUS-CPU-09-1

*Gold candidate: Aringon_01*

[TODO]

---

### 4.2 PAL

#### NUS-CPU(R)-01

*Gold candidate: Prominos_R01*

[TODO -- French PAL. S-RGB A encoder. NUS-001(FRA) exclusively.]

---

#### NUS-CPU(P)-01

[TODO -- DENC-NUS. PAL-exclusive. BU9480F retained (DENC does not integrate audio).]

---

#### NUS-CPU(P)-02

[TODO]

---

#### NUS-CPU(P)-03

[TODO -- No board image available. Entry is a stub pending source material.]

---

#### NUS-CPU(P)-03-1

[TODO -- One board image available; stamp codes illegible. MX8350 present.]

---

### 4.3 PAL-M

#### NUS-CPU(M)-01

*Gold candidate: pending (grav)*

[TODO]

---

#### NUS-CPU(M)-02

[TODO]

---

#### NUS-CPU(M)-03

*Gold candidate: Lima112_01*

[TODO]

---

#### NUS-CPU(M)-04

[TODO -- No board image available.]

---

#### NUS-CPU(M)-05

[TODO -- No board image available.]

---

#### NUS-CPU(M)-05-1

*Gold candidate: Mielke_01*

[TODO]

---

### 4.4 Engineering Samples

#### NUS-CPU-E7I

[[TODO -- Non-retail engineering sample. Board marking NUS-CPU-E7I. Serial: 32 only. Untextured shell consistent with prototype tooling. Crystal stamps: D143A6 / D147A6 (Jan 1996 / Jan 1996). Source: KontrolledKhaos_01 (AssemblerGames, Aug 2016). Photos recovered at full quality via ~29 GB archive.org WARC file of assemblergames.org from 2018.]]

---

## 5. Production Evidence

### 5.1 PCB Date Codes

[TODO -- Decode convention. Dot matrix pattern. Horizontal line interpretation (unresolved). Utility as a sorting key independent of crystal corpus.]

### 5.2 IC Date Codes

[TODO -- YYWW convention (NEC, general). Manufacturer-specific variants. How these bracket component transitions independently of board revision markings.]

### 5.3 Crystal Corpus

[TODO -- Cross-reference to timing reference §3.5.1.2 for full stamp code table. Summary of what the corpus tells us about production chronology here.]

### 5.4 Component Transition Brackets

[TODO -- CPU-NUS to CPU-NUS A bracket. MX8330MC to MX9911MC bracket. VDC-NUS path to single-chip path bracket. RDRAM18-NUS to RDRAM36-NUS bracket. Each bracket derived from earliest/latest known datecodes for each variant across the full corpus.]

---

## 6. Sources

### 6.1 Figures

[TODO]

### 6.2 References

[TODO]

### 6.3 Acknowledgements

[TODO]

---

## Glossary

[TODO]
