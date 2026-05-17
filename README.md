# kr-신화

An ontology-based digital infrastructure for Korean mythology — anchored on **무속신화** (shamanic narratives) — designed to be citation-traceable, variant-preserving, and bilingual (Korean primary, English layer).

> Tolkien's complaint was not that England had no mythology — it had Beowulf and Arthur — but that English-language pagan soil lacked a connected, accessible body. The Korean parallel is sharper: **Korea has a deep narrative core in 무속신화, but no shared, accessible, ontologically-structured canon that creators or researchers can reference.** That gap is what this project fills.

Created: 2026-04-28
Last revised: 2026-04-28 (post-adversarial-review)

---

## 0. Conventions

### Language

- **Working language: English** (prose, schema docs, commit messages, methodology notes).
- **Korean preserved verbatim** for: 신격·의례·지역·본풀이 names (바리공주, 차사본풀이, 진오귀굿, 시왕…), untranslatable concepts (한, 원혼, 굿, 본풀이), direct quotations from Korean sources.
- **First-use gloss only**, e.g., 바리공주 (Princess Bari, the psychopomp deity). Korean term stands alone afterward.
- **Source quotations**: keep original language; bracketed English gloss optional. Don't paraphrase Korean sources into English in primary notes — drift on folkloric terms is exactly what this project resists.
- **Ontology IRIs**: Korean instance names (`:바리공주 a :Deity`); class names in English (`Deity`, `Narrative`, `Ritual`).

### Source capture (citation-grade)

Every factual claim carries **author, title, publisher/journal, year, URL, page, source tier**:
- **T1** primary 무가 transcripts (현용준, 임석재, 김헌선)
- **T2** peer-reviewed (KCI, DBpia)
- **T3** encyclopedic (한국민족문화대백과, 한국민속대백과)
- **T4** popular (신동흔 대중서, news)
- **T5** excluded from canon (환단고기, 부도지, 신민족주의 재구성) — cited only as objects of study, never as fact-sources

Variants (region, informant, recording year) recorded when relevant. Web pages get retrieval dates. Ontology triples ideally carry a `:source` predicate. Full rule: `feedback_source_capture.md` in memory.

---

## 1. Problem statement

- Korea has a rich **narrative mythological core** in 무속신화 (서사무가) — 바리공주, 제주도 본풀이 12편, 창세·차사·세경 무가 등 — recorded in 20th-century fieldwork (현용준, 임석재, 김헌선, 서대석).
- Korea also has a **political/national mythological core** in 건국신화 (단군·동명·혁거세·해모수). This project **does not** treat the two as interchangeable; it works on the narrative core.
- Pseudo-canonical 야사 like 환단고기 are **rejected by majority scholarship** as 위서 (T5: 1979 first appearance, original missing, modern Sino-Korean compounds 이념·대륙·광명 anachronisms).
- Since 검은 신화: 오공 (서유기-based, 2024) demonstrated the global appetite for Asian mythology IP, Korean studios (매드엔진 「프로젝트 탈」, 넥슨게임즈 「우치 더 웨이페어러」) have started mining 한국 설화 IP — **but each project rebuilds source curation from scratch**.
- The actual missing piece is not "Korean mythology IP." It is a **shared, accessible, ontologically-structured, citation-traceable canon** that creators, scholars, and educators can reference. That is the gap kr-신화 fills.

## 2. Core sources (verified)

### 2.1 무속신화 — the narrative core

- **바리공주 (바리데기)**: psychopomp origin myth; recited in 진오귀굿/오구굿; 무조신 (founding deity of shamans).
- **제주도 본풀이 12편 (일반신본풀이)**:
  - 천지왕본풀이 (cosmogony — 대별왕/소별왕 split into 저승/이승)
  - 삼승할망본풀이 (childbirth)
  - 마누라본풀이 (smallpox)
  - 초공/이공/삼공본풀이
  - **차사본풀이** (origin of 강림도령 as 저승차사)
  - 세경본풀이 (agriculture)
  - 지장본풀이 / 문전본풀이 / 칠성본풀이 / 군웅본풀이

Note: 무속신화 is the **narrative** core in mythological scholarship (서대석, 조동일, 신동흔, 현용준 consensus). It is *not* the political-identity core — that role is played by 건국신화. The two are complementary; this project scopes to the former.

### 2.2 Primary academic infrastructure

- 한국학중앙연구원 — 한국민족문화대백과사전 (encykorea.aks.ac.kr) [T3]
- 국립민속박물관 — 한국민속대백과사전 (folkency.nfm.go.kr) [T3]
- AKS 디지털인문학연구소 — RDF/OWL semantic Korean studies data (digitalhumanities.kr)
- 한국콘텐츠진흥원 — formerly 문화원형 디지털콘텐츠 사업; rebranded post-2015 into 콘텐츠IP / 스토리텔링 lines

### 2.3 Reference scholarship (curated starting set)

- 신동흔 — 『살아있는 한국 신화』 [T4 popular standard]
- 서대석 — 한국 무가 사설 연구 [T2]
- 조동일 — 『한국문학통사』 (구비문학 sections) [T2]
- 현용준 — 『제주도 무속 자료사전』 [T1, the field's primary record]
- 박종성 — 바리공주 연구 계열 [T2]
- 김헌선 — 한국 창세신화 자료 [T1/T2]

## 3. Distinctive emphases (with East Asian comparanda)

These are not unique-to-Korea features — most have analogues in Japanese, Chinese, or Tibetan traditions — but they form a **distinctive emphasis pattern** in 무속신화 relative to Greek/Roman or Christian frames a Western-trained reader is likely to start from. Rows now flag the East Asian comparanda explicitly to avoid overclaim.

| Element | 한국 무속 | Comparanda |
|---------|-----------|------------|
| Human → deity | Mortals (당금애기, 바리, 할락궁이) become gods after trial | Comparable in 일본 신토 (人 → カミ), 도교 八仙. **Distinctive emphasis**, not unique. |
| Deity imperfection | 천지왕 fails to punish 수명장자, conceives with a mortal woman | Less prominent in Greek/Christian frames; comparable to East Asian tianming-vulnerable 天 traditions. |
| Underworld topology — horizontal strand | 저승 reachable on foot, parallel to 이승 (per 바리공주) | This is **one strand**. The 시왕 (Ten Kings, Buddhist syncretism) and 천상 strands are vertical. Korean cosmology contains both. |
| Underworld disposition — return-home strand | 저승 as 본원/이상향, 순환적 내세관 in earlier substrate | 한국민족문화대백과 「지옥」 confirms 무속 substrate has weak 지옥 concept. **But: "원형" is itself a 1970s–80s 민속학 reconstruction** — we have no pre-Buddhist 무속 texts. |
| Death handling | The dead must be **escorted**; failure → 귀신 | Holds for the 객귀/원혼 type specifically; 한국 귀신 vocabulary also covers 산신령, 도깨비, 신장 (separate categories). |
| Female psychopomp | 바리공주 — abandoned seventh daughter | Most psychopomp roles globally are male (Hermes, Charon, Yama). East Asian afterlife-adjacent female figures exist (西王母, 媽祖) but none performs the active escort function 바리 does. **Distinctive emphasis.** |

## 4. Etymology

- **저승** = 「져(저, that)」 + 「生(생/승, life)」 → "the other life/world". Validated as 다수설 in 한국민족문화대백과, 우리역사넷 [T3]. Minor dissent (native-Korean root for 승) exists but is not prevailing.
- **이승** = 「이(this)」 + 「生」.
- Later sinographic re-spelling adopted Buddhist 「乘」 — orthographic, not etymological.

## 5. The afterlife and the ghost — qualified

The user's intuition that 저승 is not inherently fearsome and that 귀신 means "stuck soul" is substantively correct, with these qualifications:

1. **"두려움의 대상 아님"** — true for the **무속 substrate strand**, where 저승 is 본원 and the dead are guided to a place. The substrate is reconstructed from 20th-century recordings and is a **scholarly model**, not a recovered pre-Buddhist text. After Buddhist 시왕 syncretism, 지옥 absolutely figures in folk-religious imagination.
2. **"가야만 할 곳"** — yes, escort/guidance is the structural role of 바리공주 and 차사 narratives.
3. **귀신 ≠ Western ghost** — true *for the 객귀 / 원혼 type* (souls stuck due to failed escort, grievance, missed 제사). 한국 귀신 vocabulary also includes 산신령 (mountain spirits, never human-derived), 도깨비 (a separate creature class), 신장 (Buddhist guardians). The user's distinction is correct as a contrast to "ghost = evil entity," but it is not a complete typology.
4. **Ritual response: "넋을 위로해 보낸다"** — pattern visible across 씻김굿, 진오귀굿, 오구굿, 49재.

The frame Christianity/secular-modern Korean discourse imports flattens (3) — turning 객귀 (a help-needed state) into ghost-as-evil. That conceptual flattening is exactly what this project pushes back on by preserving Korean-language source distinctions.

## 6. 환단고기 disposition

- **Verdict: T5, excluded from canon as fact-source.** 학계 다수설 = 위서. 1979 first appearance, original manuscript missing, modern Sino-Korean compounds (이념·대륙·광명) anachronistic ([encykorea T3](https://encykorea.aks.ac.kr/Article/E0064977)).
- The ontology will model 환단고기 류 only as **objects of post-1980 reconstruction movements**, with explicit `:movementSource` distinct from `:scholarlySource`.

## 7. Ontology

### 7.1 Definitions used

- **Philosophical**: ontology = the study of what exists and what categories of being there are.
- **Information-science** (Tom Gruber): "*An explicit specification of a conceptualization*" — formal representation of a domain via classes, properties, relations. Implementable in RDF/OWL.

### 7.2 Why ontology suits this project (and where it gets hard)

Suits:
- Mythological narratives decompose naturally into 신격, 인간, 장소, 사건, 의례 → S-P-O triples.
- Comparative mythology (mapping to Greek/Norse/Chinese analogues) becomes queryable.
- CIDOC-CRM (cultural-heritage standard ontology) is interoperable.

Hard parts (not fatal, but require design effort):
- **Variant management** is a known challenge for narrative ontology. 무가 has *regional* variants (제주 vs 함경 vs 호남), *informant* variants (different 무당 give different recitations), and *performance* variants (each 굿 enactment is unique). Reducing to triples without a variant model collapses what makes the tradition distinctive.
- **Solution direction**: each `Witness` instance is a recorded transcript with `:region`, `:informant` / `:performer`, `:recordingYear`, `:performanceContext`. Avoid a "main version" anti-pattern. Variant preservation is a methodological selling point in NRF/AKS proposals.
- **Performance ontology**: PROV-O + CIDOC-CRM `E7_Activity` handle the "굿 as event" dimension; aligned in v0 (see `v0_specification.md` Deliverable 3a).

### 7.3 Top-level classes (draft v0.1)

```
Deity              # 천지왕, 바리공주, 강림차사
Human              # 수명장자
Spirit             # 객귀, 원혼, 잡귀 (subclasses to be elaborated)
NonHumanEntity     # 산신령, 도깨비, 신장 (separate from Spirit per §5)
Realm              # 이승, 저승, 서천꽃밭
Narrative          # a witnessed variant of a 본풀이/무가
NarrativeFamily    # the abstract narrative family that variants instantiate
Ritual             # 굿 type (오구굿, 시왕맞이)
RitualEnactment    # a specific performance instance, when relevant
Region             # 제주, 함경, 호남, 평안 (with hierarchy)
Source             # bibliographic record (per §0 source-capture rule)
ReconstructionMovement  # 1980s+ 신민족주의 / 신흥종교 frames; tagged distinct from scholarly sources
Comparison         # cross-mythology mappings
```

### 7.4 Predicate examples

Stable IRI namespace: `https://w3id.org/kr-shinhwa/` (per `v0_specification.md` Deliverable 2).

```turtle
@prefix kr: <https://w3id.org/kr-shinhwa/> .
@prefix crm: <http://www.cidoc-crm.org/cidoc-crm/> .
@prefix prov: <http://www.w3.org/ns/prov#> .
@prefix dcterms: <http://purl.org/dc/terms/> .

kr:바리공주_김금화_1972 a kr:Witness , crm:E73_Information_Object ;
   kr:memberOf kr:바리공주 ;       # NarrativeFamily
   kr:region kr:황해도 ;
   kr:informant kr:김금화 ;
   kr:recordingYear 1972 ;
   kr:recordedBy kr:서대석 ;
   kr:ritualContext kr:진오귀굿 ;
   kr:majorDeity kr:바리공주 ;
   prov:wasDerivedFrom kr:seo_daeseok_1980 ;
   dcterms:source kr:seo_daeseok_1980 .

kr:바리공주 a kr:Deity ;
   kr:gender "female" ;
   kr:role kr:PsychopompFunction ;
   kr:foundIn kr:진오귀굿 , kr:오구굿 .

kr:환단고기_재구성 a kr:ReconstructionMovement ;
   kr:firstPublished 1979 ;
   kr:scholarlyStatus "rejected_majority" ;
   dcterms:source kr:encykorea_E0064977 .
```

## 8. Phased plan

The operational document is `roadmap.md` (week-by-week) and `v0_specification.md` (the focused build document for v0). Summary:

**Phase 0 (v0, by end June 2026)** — see `v0_specification.md` for the 13 deliverables. Subject: **차사본풀이 only** (one narrative family modeled deeply, in a way that makes it the prototype for the rest). Deliverables include the ontology (CIDOC-CRM + PROV-O + FOAF + Dublin Core aligned), a SKOS thesaurus, a TEI envelope, a SPARQL endpoint, a Data Management Plan, MARC record, Zenodo DOI, three audience-tailored methodology one-pagers, and bilingual structured summary. Effort estimate: 80–110 focused hours.

**Phase 1 (Jul–Dec 2026) — horizontal expansion**
- Add 바리공주 (3 regional variants), 천지왕본풀이, then 세경본풀이 / 삼승할망본풀이.
- Each new family is an instance addition to the same v0 ontology, not a schema rewrite.
- Outreach: KADH 가을 학술대회 talk, AKS DH Institute newsletter pitch, Open Knowledge Korea / Code for Seoul demo, LOD-Cloud submission.
- Grant applications: SFAC 청년예술지원 (Sep–Oct 2026), AKS 한국학대형기획총서 (Aug–Oct 2026 via institutional partner), Wikimedia Rapid Fund (Nov 2026).

**Phase 2 (Jan–Apr 2027) — v1 milestone**
- v1 = 5 narrative families fully modeled, sources.bib ≥80, Wikidata ≥30 sourced statements, methodology paper draft, NEH Public Scholars Chapter 1 draft.
- Grant applications: SFAC RE:SEARCH (Feb 2027, subject to simultaneous-selection prohibition).

**Phase 3 (May 2027 – Apr 2028) — scale**
- NEH Public Scholars (Sep 2027 cycle, US side, requires v1 + writing sample).
- KF #13 librarian outreach wave 2.
- AKS 한국학기초자료사업 신규과제 (2028 cycle, ₩1.2–1.5B / 3+ yrs) once track record is established.
- Studio engagement: position as *consulting + structured-data subscription*, not license sale (fact data has weak copyright; protectable value lives in curation/structure).
- Popular book in the 신동흔 successor lineage.

## 9. Beneficiaries

- **Creators** (game studios, novelists, animators) — stop rebuilding source curation each project.
- **Researchers** in 무속학·민속학·비교신화학 — shared computable infrastructure.
- **Education** — schools get a structured, navigable Korean mythology resource.
- **Diaspora and global K-content audiences** — bilingual layer makes Korean shamanic mythology globally citable for the first time.
- **The maintainer (you)** — authority position as the curator of the standard.

## 10. Revenue posture (revised)

| Model | Realism | Note |
|-------|---------|------|
| Korean public funding via affiliation (AKS 한국학대형기획총서 ₩60M/2yrs Aug–Oct 2026; SFAC 청년 ₩10M Sep–Oct 2026; SFAC RE:SEARCH ₩3M Feb 2027) | High | All gated by v0 ship (June 2026) — see `v0_specification.md`. First 2–3 years of work plausibly lives here. KF is indirect-only; NRF gated until PhD/affiliation. |
| KF #13 한국연구자료지원 (전자) via overseas KS librarians | Medium-high indirect | US$5K/library/yr at 50% match. Gated by v0 Zenodo DOI + MARC record (Deliverable 10). Outreach Jul–Sep 2026. |
| Popular book (신동흔 lineage) | Medium-high | Tolkien-Silmarillion analogue. NEH Public Scholars (US side, Sep 2027 cycle) supports this directly; bilingual narrative-episode summaries (class deferred to v0.5; v0 Deliverable 6a) are the writing-voice prototype for Chapter 1. |
| B2B consulting + structured-data subscription | Medium | Studios buy the *curator*, not the *facts*. |
| Public visualization site (traffic / sponsorship) | Low-medium | Cumulative. |
| Direct game/anime IP development | Low (alone) | Capital-heavy; partner required. |
| **"K-mythology canon" authority position** | **High authority, low direct revenue** | Convertible to consulting, advisory roles, conference circuit, government committee seats. Standards-body model (W3C/Unicode), not Disney IP model. |

Direct license revenue from "Korean canonical mythology" requires a producer partner (studio, publisher, broadcaster). Without that, the play is **authority → consulting/grants/publication**, which is durable and academically credible.

## 11. Why this is cosmology, not folk-curiosity

한국 무속신화 forms a complete cosmology — **창세 → 인간 → 죽음 → 사후 → 재생** — with differentiated relations among 신·인간·귀신·저승. The reason it gets called 미신 in modern Korean discourse is not that it lacks coherence; it's that:

1. It was **never canonized** in the way *Edda* canonized Norse myth or *Theogony* canonized Greek myth. Coherence is distributed across regional 무가, never collected under one editor — **and would not be**, since regional/performative variation is constitutive of the tradition (see §12). The project is not Snorri-style canonization; it is structured navigability over the documented record.
2. **Christianity, secular-modern education, and 신민족주의 환단고기 류 reconstruction** have each, for different reasons, displaced the substrate from contemporary self-understanding.
3. **Lack of an accessible, structured, citation-grounded reference** keeps it outside of formal teaching, despite its richness.

This project addresses (1) and (3) directly. It does not try to "restore" a pre-Buddhist substrate — that would be the same epistemological mistake 환단고기 makes in the other direction. It curates what is documented, models variants honestly, and makes the documented material navigable.

## 12. Variant preservation is a first principle

A "single canon" of Korean mythology, in the Snorri-edited Norse model, would erase exactly what makes the tradition distinctive. The ontology preserves variants as first-class data:

- Each `Narrative` instance is a **witnessed variant**, not a normalized version.
- `NarrativeFamily` groups variants without privileging one as authoritative.
- `:region`, `:informant`, `:recordingYear`, `:performanceContext` are required predicates for narrative instances.
- Comparative views aggregate across variants explicitly, never silently.

This is also the project's strongest methodological selling point in NRF/AKS proposals: *we are not making up a canon, we are building queryable infrastructure over the documented record while preserving its multiplicity*.

---

## Sources (validated round 1)

- [Etymology — 이승과 저승, 우리역사넷](https://contents.history.go.kr/front/km/view.do?levelId=km_005_0030_0020) [T3]
- [바리공주 — 한국민족문화대백과사전](https://encykorea.aks.ac.kr/Article/E0020479) [T3]
- [바리공주 — 한국민속대백과사전](https://folkency.nfm.go.kr/topic/detail/2132) [T3]
- [천지왕본풀이 — 한국민족문화대백과사전](https://encykorea.aks.ac.kr/Article/E0056050) [T3]
- [차사본풀이 — 한국민족문화대백과사전](https://encykorea.aks.ac.kr/Article/E0055151) [T3]
- [한국 신화의 특징 — AKS 웹진 2204](https://www.aks.ac.kr/cefia/webzine/2204/focus.html) [T3]
- [한국 무속과 민간불교의 혼합현상 — SNU 종교학논집](https://s-space.snu.ac.kr/bitstream/10371/5169/3/religiousstudy_v24_073.pdf) [T2]
- [〈바리공주〉의 여성신화적 성격 연구 — SNU](https://s-space.snu.ac.kr/bitstream/10371/4685/3/ReligionandCulture_v10_21.pdf) [T2]
- [지옥 — 한국민족문화대백과사전](https://encykorea.aks.ac.kr/Article/E0054310) [T3]
- [환단고기 — 한국민족문화대백과사전 (위서 다수설)](https://encykorea.aks.ac.kr/Article/E0064977) [T3]
- [Ontology — Wikipedia (philosophical)](https://en.wikipedia.org/wiki/Ontology) [T4]
- [Ontology (information science) — Wikipedia](https://en.wikipedia.org/wiki/Ontology_(information_science)) [T4]
- [Tom Gruber — Definition of Ontology](https://tomgruber.org/writing/definition-of-ontology/) [T2]
- [Ontologies for Cultural Heritage — Springer](https://link.springer.com/chapter/10.1007/978-3-540-92673-3_21) [T2]
- [AKS 디지털인문학연구소](https://digitalhumanities.kr/) [T3]
- [Digital Humanities Series — Ontology (wikidocs)](https://wikidocs.net/179934) [T4]
- [K-IP 동향 post 검은신화: 오공 — 시사저널e](https://www.sisajournal-e.com/news/articleView.html?idxno=416328) [T4]

Companion files: `funding.md` (funder landscape), `adversarial_review.md` (claim-by-claim verdicts), memory in `~/.claude/projects/.../memory/`.
