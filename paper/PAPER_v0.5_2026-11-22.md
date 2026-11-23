---
title: "Choosing What to Collect: Deliberate Selection Against Indiscriminate Pulling, and a Source-Checked Delineation of Open Archives to Pick, Hold, Refuse and Retire"
author: "Aaron Michael Weis (ORCID 0009-0002-1906-148X), Oneiron Holdings LLC, Denver, Colorado, USA"
date: "22 November 2026, version 0.5"
subject: "Dataset selection, provenance, licensing and retirement"
keywords: [dataset selection, data provenance, data poisoning, open data, licensing, data retirement]
---

# Choosing What to Collect: Deliberate Selection Against Indiscriminate Pulling, and a Source-Checked Delineation of Open Archives to Pick, Hold, Refuse and Retire

**Aaron Michael Weis · Oneiron Holdings LLC · 22 November 2026 · v0.5**

**Scope.** This preprint presents a method for choosing public records against a written research goal. The initial survey used search extracts and page summaries. Section 12.6 identifies the individual claims checked against publisher pages for this edition. The proposed collection tests remain open. Earlier decisions that changed during drafting are marked *superseded* in the text.

# Abstract

Which records are worth collecting for a particular research question? This paper proposes writing down the question first, then inspecting each candidate’s provenance, rights, and relevance. Four strands of published work motivate the approach. A small number of harmful records affected models of several sizes in one controlled study. A licensing audit documented missing and incorrect labels. Experiments on repeated training with model-generated data found a loss of diversity under the conditions studied. Research on Common Crawl documented how its collection practices shape coverage. Using public archives as examples, the paper distinguishes sources suitable for narrow collection, sources to hold for review, and sources to decline. It also sets out how to propose retiring a record and trace the copies that depend on it. The author proposes four tests of the method. This edition reports a literature and policy review and a replay of the evidence tools. No dataset was collected and the four tests have yet to be run.

**Keywords:** dataset selection; data provenance; data poisoning; open data; licensing; data retirement.

# 1. Introduction

A common way to build a data set is to take all that can be taken. A crawler follows every link. A team downloads the largest public dump on the grounds that it is large. Further along the same road, a party with access takes the working files, messages or ideas of the people it serves and treats them as raw material. The shared habit is that the collector begins from what is reachable and decides later what it is for.

This paper takes the opposite position, and states it as the author's position rather than as a finding. The records worth having are the ones that bear on a goal written down before collection starts. Collecting without a goal defers the only hard decision, and the pool then holds too many unrelated, unlicensed or unwanted records to examine. And when what is taken was never offered (private messages, unpublished projects, ideas shared in confidence) it is also, in the author's view, ethically unsound, whatever the pool later yields. Filters and sorting tools may help at the margin; they cannot supply the goal.

The practical argument is that unexamined volume is a liability. Section 4 summarises four bodies of work that bear on it. Section 5 applies the argument to a supplied list of public archives that the list's author described as under-used. Section 6 proposes what may be retired. Section 7 gives the admission graph. Section 8 states four tests. Section 9 states what this study did not do. Section 11 (added in v0.2) corrects the CERN entry, adds further candidate sources, sets out a cleaning route that uses only local programs, and describes the audit record. Sections 11.7 to 11.10 (added in v0.5) read seven further sources in four families (arXiv bulk data and LaTeX source, figshare, CSIRO, and four municipal portals) against their own pages. Section 12 (added in v0.4, repeated in 12.5) reports a run of the author's own receipt tools on this paper, and Section 13 tabulates the residual risks and the gate that answers each.

# 2. Definitions

**Goal row.** A one-sentence statement, written before any pull, of which question, claim or test a record will feed and what it adds that is not already held.

**Cherry-picking.** Selection of records against a goal row, from sources whose terms permit the use, in a quantity small enough to read.

**Siphoning.** Collection of records from a party that did not offer them, or from a system the collector was not given the right to read for that purpose. The term is used here for the practice, not for any named incident, and no statement in this paper depends on a specific event.

**Dark or long-tail data.** Records that are held openly but rarely read. The supplied list asserts that large archives are largely untouched; this paper did not measure access and treats the assertion as unverified.

**Quarantine.** A holding area where a record is hashed, checked against its card, and not used until it passes.

**Retirement.** Removal of the author's own copy of a record from active use. In this paper retirement is proposed, never performed, and never reaches a record's ledger entry.

**Poison.** A record that, if learned from, causes behaviour the collector did not intend, by design or by accident. This includes malicious records, mislabelled records, and unmarked model-generated text.

# 3. Sources and verification

The supplied list (held by the author) names a set of archives and techniques. Each was read against the archive's own policy or documentation page, or against a study of it, through 19 standard web searches on 22 November 2026. Each search returned extracts; no page was opened in full, and the sources added in Sections 11.7 to 11.10 were read as summaries from a page-fetch tool. A claim row records what the extract said, the source, a falsifier, and a provisional grade; the grade validator was not run. Where the extracts did not reach a primary page, the entry says so, and absence is stated with its bound ("not found within this budget") rather than as absence. Sources outside the archive's own host are marked as secondary.

The author's position (Section 1) and the proposals (Sections 5 to 7) are not findings and carry no grade.

# 4. Why unexamined volume costs more than it yields

## 4.1 A small, fixed number of records can matter

A controlled study found that a small set of harmful training records could affect the behavior of models across the range of sizes tested [1][2]. The study examined a narrow, low-stakes behavior. It did not establish how often this happens in existing archives or across other model behaviors. For a collector, the practical question is how to recognize a consequential record when the collection as a whole looks ordinary. Section 8 proposes tests of a selection rule built around that question.

## 4.2 Licenses and provenance are often wrong in the places people look

An audit by a multidisciplinary group traced more than 1,800 text data sets and reported license omission above 70% and error rates above 50% on widely used hosting sites [3]. The study concerned fine-tuning data sets and was published in 2024, so it does not describe the archives in Section 5. It does show that a stated license on a hosting page is evidence to be checked, not a fact.

## 4.3 Unmarked synthetic text degrades what learns from it

A peer-reviewed study found that indiscriminate use of model-generated content in training causes irreversible defects, in which the tails of the original distribution disappear [4]. An author correction was published in 2025 [5], and a later note argued the outcome is a statistical phenomenon [6]; the finding is cited here for the narrow point that unmarked generated text is a contaminant to be tracked, not for its size.

## 4.4 The largest public crawl is deliberately uncurated

Common Crawl states a total archive above 10 petabytes collected since 2008, with monthly crawls of more than two billion pages [7]. A 2024 study for the Mozilla Foundation reports that it is neither the whole web nor a representative sample, and that builders commonly filter it before training, because the archive does not curate [8].

## 4.5 Reading of the four

None of the four is a result about every collection, and none shows that goal-directed selection yields better systems; that is a test (Section 8). Together they support a narrower claim: examination cost per record is not avoidable by collecting more, and a pool without goal rows has no standard to examine against.

# 5. The delineation list

Table 1 sorts each source in the supplied list into one of three proposed decisions (pick narrowly, hold, do not pick); Section 6 treats retirement separately. The decisions are proposals for the author's ruling. "Pick" means: admit narrow slices that pass the gates in Section 7 and have a goal row. It does not mean bulk download.

| Source (as named in the supplied list) | What the pages read say | Proposed decision |
|---|---|---|
| NASA Earthdata | Data from NASA-led missions are licensed CC0 unless marked with a restriction; citation is urged; the system holds more than 120 petabytes [9] | Pick narrowly: one collection at a time, with its DOI |
| NOAA Open Data (cloud program) | More than 24 PB made public through three cloud providers; a listing states the data are open to the public and usable as desired [10][11] | Pick narrowly: named datasets only |
| CERN Open Data Portal | CC0 for the data, DOIs, no endorsement by CERN; more than 5 PB; the portal focuses on event data of levels 2 and 3 [12][13][14], and a secondary report of the policy says raw data is generally not released [35] | Pick narrowly from levels 2 and 3 only. The list's "raw collision data" description does not match. *SUPERSEDED in part by v0.2 (Section 11.1): the portal also carries 2024 to 2026 releases, from earlier collision years in the extracts read.* |
| Library of Congress HAER | Original drawings were created for the US Government and are generally public domain; images copied from other sources may be restricted [15] | Pick narrowly, item by item, reading each item's rights advisory |
| Pre-1929 engineering handbooks (HathiTrust, Internet Archive) | In the United States, works from 1930 entered the public domain on 1 January 2026 [16]; HathiTrust forbids automated bulk download except through its own products [17]; the Internet Archive gives no guarantee of copyright status [18] | Pick narrowly by hand or through an approved product, with the date rule updated to 1930. No scripted bulk download |
| Software Heritage | The archive holds about 9 billion unique files and 2 billion commits from about 150 million repositories [19]; its bulk terms say extracted material is used under each component's own license [20] | Hold: admit per repository after a license check. Not wholesale |
| Common Crawl | See 4.4; the terms page was not read | Hold: admit only a documented, filtered derivative, never the raw archive |
| NASA Technical Reports Server | Documents are not under copyright unless noted, but some were contributed by private parties; a 2013 takedown followed concerns about export-controlled items [21][22] | Hold: per-document copyright flag required |
| Breakthrough Listen | About 1 PB in its first release; filterbank files of several gigabytes needing specialised software; license text not found in the extracts [23][24] | Hold until the license is read. Slices only, if admitted |
| IETF Internet-Drafts (expired) | Drafts are to be cited only as work in progress and had a nominal life of about six months; they remain in a public archive and fall under the IETF's legal provisions [25][26] | Hold: published RFCs may be picked; expired drafts need the legal-provisions check and a goal row |
| openFDA device clearances | The interface returns details about products and sponsors, monthly, with a notice that results are unvalidated [27][28]; the summary documents were not reached | Hold: use as an index. The claim that it returns engineering specifications is not supported by the pages read |
| Zenodo, Figshare, Data.gov, municipal portals, DTIC, CSIRO | Not checked within this budget. *SUPERSEDED in part by v0.5: Figshare, CSIRO and four municipal portals were read (Sections 11.7 to 11.9). Zenodo, Data.gov and DTIC remain unchecked.* | Hold: unchecked is not admitted. For the families now read, see Table 5 |
| arXiv LaTeX source, "commented-out" text | The default license gives arXiv a non-exclusive right and grants readers no reuse right; reuse needs the author's permission unless a Creative Commons license was chosen; metadata is CC0 [29][30]; automated downloads outside its bulk routes are not permitted [31][32] | Do not pick author comments, which are unpublished notes. Pick text only of papers carrying an open license and only through the bulk route. *Expanded in v0.5 (Section 11.7).* |
| Open directory listings on lab and observatory servers | Not checked against any policy; the list gives no license for such files | Do not pick: unlinked files may be unpublished or private |
| GrabCAD, Thingiverse models | GrabCAD tells members to obtain the designer's explicit permission and attribute [33]; Thingiverse widened its per-upload license choices in April 2026 [34] | Do not pick in bulk; per-model, with the designer's permission |
| Git "removed" and "reverted" history | Not checked | Do not pick until license and secret checks exist; code is often removed for reasons |
| Any message, project or idea taken without being offered | Not an archive; position stated in Section 1 | Do not pick, whatever the volume |

*Table 1.* Proposed decisions. Bracketed numbers refer to the reference list.

## 5.1 Statements in the supplied list that the pages read did not confirm

1. "Over 18 billion unique source files" in Software Heritage. A 2026 study reports about 9 billion; no page read gave 18 billion. The live counter was not read [19].
2. "Pre-1929" for public-domain engineering handbooks. The United States boundary moved to works published in 1930 on 1 January 2026 [16].
3. The openFDA 510(k) interface returns "engineering specs of diagnostic hardware". The pages read describe product and sponsor details [27].
4. CERN "raw particle collision datasets" sit idle. The portal focuses on levels 2 and 3, and a secondary report says raw data is generally not released [14][35]. *Note added in v0.2: the author observed that CERN did release data in 2024 and 2025, which the extracts confirm (Section 11.1); the point here is about raw data and about the most recent run, not about whether releases exist.*
5. Breakthrough Listen's data are in ".fil or .fits" slices. The extracts describe filterbank products moving to HDF5; ".fits" was not found.
6. "99.9% of the raw data" is archived untouched; hundreds of petabytes "never downloaded"; archives "receive almost zero traffic". No page read measured access; unverified.

# 6. Retirement

Retirement answers a different question from admission: of what is already held, what leaves active use. The proposals below are for the author's ruling; nothing is deleted by this paper or by any tool it describes.

**Proposed for retirement (own copies only):**

- records with no goal row, after a stated waiting period;
- exact and near duplicates, keeping one with its ledger entry;
- records whose license is missing, unreadable or in conflict with its page;
- records that failed a gate and remain in quarantine;
- personal-data shapes found by a count-only scan, with matches never stored;
- records of unknown or model-generated provenance that cannot be marked;
- records taken without being offered, and any derivative of them.

**Never retired by this process:** the ledger entry of any record, its hash, its card, its takedown record, and any quarantine report. A retired record can be explained afterward.

**Order.** Reversible first: move to a read-only archive, verify that nothing in active use depends on it, wait, then let the author decide on deletion. Any deletion happens by the author's hand.

# 7. The admission graph

Every record travels the same directed acyclic graph. A record never returns to an earlier node; a failed record is re-submitted as a new candidate with a new goal row.

| Node | What it is | Leaves to |
|---|---|---|
| N0 Goal row | Written sentence naming the claim or test fed | N1 |
| N1 Candidate | Source named, with its policy page | N2, or end (no policy page) |
| N2 Card check | License, provenance, collection window, personal-data statement, takedown route, read from the source | N3, or end (no license) |
| N3 Small-sample probe | A few records read by a person; secret and personal-data shapes counted; card compared with sample | N4 if the sample matches; hold if not |
| N4 Quarantine | Hashed, read-only, ledger entry opened | N5 |
| N5 Cleaning | Duplicates counted, hidden characters and agent-addressed lines flagged as data not instructions, label audit on a sample | N6, or end; a failed record is resubmitted as a new candidate at N0 |
| N6 Admit | Ledger entry closed with the author's yes | N7 |
| N7 Use | Fed to the stated claim or test only | N8 |
| N8 Retire | Proposed after a wait; reversible first | end |

*Table 2.* Edges of the admission graph. The only node reachable without the author's decision is N0 to N5; N6 and N8 need it.

```
N0 -> N1 -> N2 -> N3 -> N4 -> N5 -> N6 -> N7 -> N8
         \    \     \
          end  end  hold (sample does not match card)
```

# 8. Hypotheses and tests

All four are untested. No data set was pulled.

**H1.** For a fixed task and a fixed budget of records, a set chosen against a goal row outperforms a random set of the same size drawn from the same pool, on a metric fixed in advance. *Falsifier:* no difference, or a difference in the other direction, on that metric.

**H2.** In a sample of fifty candidate data sets drawn from the sources in Table 1, a large share fail the card check at N2. *Falsifier:* few fail; the proposed reading of the audit in 4.2 as applicable to open archives is then dropped.

**H3.** The probe at N3 catches mismatches between a card and its contents that a card check alone does not. *Falsifier:* every mismatch found at N3 was already visible at N2.

**H4.** Retiring records with no goal row does not change performance on the stated task. *Falsifier:* a measurable drop on the pre-fixed metric after retirement.

# 9. Limitations

## 9.1 What this study did not do

- The drafting survey used extracts and page summaries. Section 12.6 identifies the source texts checked separately for the public edition. Archive terms can change.
- No data was downloaded, sampled or scanned. No dataset was admitted.
- The grade validator was not run; grades are provisional.
- Zenodo, Data.gov, DTIC, directory-listing crawling and git deletion history were not checked. *Figshare, CSIRO and four municipal portals were read in v0.5 (Sections 11.7 to 11.9), at the level of summaries of their policy pages.*
- Terms of use for Common Crawl, Internet Archive and others were read at the level of help pages, not the full agreements.
- No lawyer has read this. Nothing here is legal advice.
- The studies in Section 4 have narrow scope (4.1 one backdoor type, 4.2 fine-tuning sets, 4.3 a stylised setting). They support a reading, not a rule.

## 9.2 Readings taken without the author's word

- The proposed screening steps can be implemented with local tools. Their accuracy on a collected dataset remains untested.
- "Delete" was read as a proposal about the author's own copies, not about any outside archive.
- "Dark data" was read as rarely read public records, not as private data.

# 11. Revision 0.2: corrections, further sources, local cleaning, audit record

Added in revision 0.2 after 9 further standard searches (28 search extracts in all for the paper at that stage). Extracts only; no page opened in full; no data pulled; grades provisional.

## 11.1 CERN: releases in 2024 to 2026, and what is not there

The author observed that CERN has data from 2024 and 2025 but, as far as he knew, not the most recent. The extracts support the first part. The portal's news list shows a CMS release of 13 TeV proton collision data from 2016 (April 2024), an ATLAS release of 65 TB (July 2024), the whole DELPHI collection (August 2024), a first TOTEM release and a first ATLAS heavy-ion release (December 2024) [36]. An ATLAS conference paper puts the research release at the full 2015 and 2016 proton data, about 45 TB, plus a 2015 lead-lead set of 221 million collisions, described as the first Run-2 heavy-ion open dataset [37]. Later items on the portal are an ATLAS education and outreach beta (July 2025), cold storage (October 2025) and an LHCb service for Run II data (February 2026) [38]. So the releases are recent; the collisions they contain are from 2015 and 2016 and earlier. Data from Run 3 (2022 onward) was not found in these extracts: *not found within this budget (9 searches; the portal's own dataset search was not read)*. The extracts neither confirm nor refute the author's belief about the newest data, and the portal's dataset pages are the place to settle it.

## 11.2 Further candidate sources

Table 3 adds sources chosen because they are not known to be widely used for training (access was not measured). Decisions follow the same three groups as Table 1.

| Source | What the pages read say | Proposed decision |
|---|---|---|
| Chronicling America (Library of Congress) | Bulk OCR downloads are offered for research [39]; the programme covers 1736 to 1963, over 23.7 million pages and 4,500 titles, per a 2026 programme slide deck [40]; a study notes content is concentrated before 1925 where it is public domain, and that its own structured extraction beat the stock OCR [41] | Pick narrowly: titles and years the goal row names, published 1930 or earlier, subject to each issue's rights note, until later issues are read; treat stock OCR as noisy |
| Public-domain newswire (1878 to 1977) | A derived set of 2.7 million articles, filtered by a classifier to newswire, which the authors treat as public domain [42] | Hold: a derivative with a classifier in the loop; read the authors' license and sample for misclassified items |
| Smithsonian Open Access | About 2.8 million 2D and 3D items and data under CC0 at the 2020 launch, with bulk download [43][45]; around 2,200 3D models in glTF [44]; the page warns that CC0 covers copyright only and other permissions may still be needed [43] | Pick narrowly: 3D models and collection metadata, item by item, reading each rights note |
| Biodiversity Heritage Library open data | All BHL data offered under CC0 1.0 in hosted and complete versions [46] | Pick narrowly: metadata and OCR for a named goal; scanned plates may carry other rights, to be read |
| Crystallography Open Database | All data and the database placed in the public domain under CC0; users are asked to acknowledge the original authors [47]; a mirror page lists 533,828 entries with a latest deposit dated 14 May 2026 [48] | Pick narrowly: structure files by goal; keep the acknowledgement |
| NASA Planetary Data System | The data.gov record gives no license, and says US-employee work is a US Government work [49]; the archive runs through seven institutional nodes [50] | Hold: license is per node and per contributor; read each node's terms |
| NIST Standard Reference Data | Free and fee-based databases; the counts differ between two NIST pages (49 free with 41 fee-based, and 49 free with 14 fee-based) [51][52]; NIST says copyright gives it tools against unauthorised use, modification or misrepresentation [52]; the WebBook record points to a NIST open license page [53] | Hold: read the license page and each database's terms; do not bulk-copy fee-based products |
| EarthScope seismic archives | Free open access to time-series data [54]; a sponsored open subset in miniSEED form [55]; some holdings have access restrictions governed by their network or program [56] | Pick narrowly: open networks only; restricted sets are not touched |

*Table 3.* Further candidates. Bracketed numbers refer to the reference list.

## 11.4 Cleaning with local programs only

The route below uses programs that run on the author's own machine, and it starts only after a record has passed N2 and N3 in Table 2. Nothing is sent to a cloud service. Each program is named as the pages describe it; none was installed or run for this paper.

| Step | Program class | Programs the pages describe | What to confirm before relying on it |
|---|---|---|---|
| Fingerprint and ledger | Hash tool | The operating system's own SHA-256 command | Same file gives same hash on two runs |
| Duplicates and broken files | Duplicate finder | Czkawka, which finds duplicate files, similar images, empty files and broken files [63] | Version and license on its page |
| Tabular cleaning | Local data editor and engine | OpenRefine, which runs a small server on the machine and keeps project data, history and preferences there; the data are not encrypted by default, so disk encryption is advised [57]; DuckDB for queries on local files | That OpenRefine is started with no extensions that call outside services |
| Personal-data scan | Text de-identification library | Presidio, open source, usable from Python or in a container, for text and images [59][60] | That its language models are fetched once and then kept offline; not confirmed |
| Secret scan | Secret scanner | Gitleaks and TruffleHog document checks for exposed credentials [61][62] | Keep local screening offline and record only counts. |
| Optional local model help | Small model run locally | A talk describes OpenRefine with a local model through Ollama, working offline [58] | Model license; a local model is a reader of untrusted text, so its output is data, not instructions |

*Table 4.* A local-only cleaning route.

A local tool can support these checks. Each record still needs a written purpose.

## 11.5 The audit record

Everything above is recorded so that a third party can verify it later. One ledger row per record, kept locally and never altered in place (a correction is a new row that points to the old one), holds:

1. the goal row it serves;
2. the source address and the UTC time of retrieval;
3. a saved copy of the license or terms text as read that day, with its own fingerprint;
4. the file's SHA-256 fingerprint and size;
5. the name and version of each program that touched it, and the settings used;
6. each gate result at N2 to N5 with the reader's initials;
7. the decision (admit, hold, refuse, retire) and the author's yes or no, dated;
8. the takedown route and any later takedown.

The proposed log links each row to the preceding row’s fingerprint. Detecting a later rewrite of the entire log requires a trusted copy of an earlier fingerprint. The record is intended to ease later review; it is not legal advice.

## 11.6 What is and is not unlocked

Nothing is unlocked by this paper. No dataset was downloaded, cleaned or admitted. What exists is a list of places that appear usable, a gate each must pass, a local cleaning route and an audit record. A derived dataset, for instance a cleaned or reformatted form of a CC0 archive, becomes a new clean dataset only after it passes the admission graph, keeps its upstream attribution, and carries a ledger row. Whether any such set improves a system is H1, and it is untested.

## 11.7 arXiv bulk data and LaTeX source

arXiv's own help pages offer four routes: a Kaggle snapshot, requester-pays Amazon S3 buckets, the OAI-PMH metadata interface and a real-time API [64]. The S3 buckets hold PDFs and source files (mostly TeX with figures) in archives of about 500 MB with checksummed manifests, about 9.2 TB in April 2025 (current size not read), growing by about 100 GB a month [65]. The scope of the Kaggle snapshot is unresolved: one page summary called it metadata plus full-text PDFs, and the Kaggle page itself did not confirm that. It is not relied on here.

On terms, the API terms of use set one request every three seconds on a single connection for the legacy interfaces, and say the limits may change [66]. The bulk page describes a looser burst pattern; the stricter terms are followed here as the cautious reading [64][66]. The same terms bar storing and serving e-prints (PDFs, source files or other material) from one's own servers unless the copyright holder or the submission's license permits, and note that only a small subset carry licenses that allow redistribution [66]. Authors choose one of six licenses per submission (CC BY, CC BY-SA, CC BY-NC-SA, CC BY-NC-ND, CC Zero, or arXiv's own non-exclusive license); different versions of one paper can carry different licenses, and the choice is irrevocable; descriptive metadata is CC0 [67]. The OAI-PMH formats carry the license; the search API does not [68]. Source is present only for the formats a submitter supplied; a TeX paper's source is a gzipped file or tar archive, and ancillary files sit in an "anc" folder per version [69]. A withdrawal adds a new version with no PDF or source link, while earlier versions stay available [70].

*Bounded negatives* (ten page reads and one search for the arXiv family): no page read addresses machine-learning use as such; none cautions about comments inside TeX files; none says whether a paper's license covers its source files, so that is inference only; whether the Kaggle snapshot has a license field per record, and the risk of duplicated or cross-listed content, were not found within this budget.

## 11.8 figshare and the CSIRO Data Access Portal

figshare's policy page (modified 11 May 2026) names two licenses for public items, CC0 and CC BY, with CC0 the default for datasets; public content can be downloaded without logging in, and bulk download or mining through the API is subject to each item's license; metadata is CC0 though client repositories may set different terms [71]. The API documentation describes no automatic limit but monitors for abuse and recommends about one request a second, caps result offsets at 1,000, and exposes the license per item and through OAI-PMH [72]. Its terms of service could not be fetched, so copyright retention is not confirmed.

The CSIRO portal holds the organisation's own research collections, from staff, collaborators and approved outside parties; collections are open or restricted at the data level, and external depositors must use a Creative Commons license, CC BY by default (plan modified 23 March 2026) [73]. Its licence page (modified 7 March 2024) lists six Creative Commons options for data, including NC and ND variants, and three retired licenses that may remain on older collections [74]; a retired CSIRO data license is non-commercial and bars sublicensing [74]. A restricted tier for specimen images needs a signed agreement and CSIRO's approval [75]. The metadata service (page modified 29 June 2026) covers metadata only; no bulk data-file route was described, and OAI-PMH is retired [76]. *Not found within this budget:* how data files are fetched programmatically, and which collections still carry the retired license.

## 11.9 Municipal open-data portals

Four portals were read at the level of their licensing and terms pages. The City of Toronto publishes under the Open Government Licence – Toronto: commercial use allowed, attribution required, and personal information and third-party rights excluded (modified 25 February 2025) [82]. New York City's overview names no open license: use is under the city's website terms and any terms an agency adds, and version history must be checked for the individual dataset [77][78]. Denver's catalog page says users may copy, distribute and adapt the data, but the page read dates in content to 2018 and may be stale [81]. Chicago's About page states no license, and its disclaimer page could not be fetched [80]. Socrata's documentation, a vendor page and not a city page, says requests without an app token share a limit by IP address and a throttled request returns HTTP 429; that Chicago and New York use that platform is inferred from page cues, not stated by the portals [79].

Several types of municipal data are not known to be widely used for training. The pages read show only that these datasets exist, by title: NYC 311 service requests [84], Chicago building permits [85], Toronto street trees (marked Retired on its page) [83]. Two further types (Chicago sensor locations through a federal catalogue copy, and Toronto transit feeds) rest on search results only and were not read. No page read described how location or free-text complaint fields are redacted; that is *not found within this budget*, and a person must read each dataset's own metadata before any 311-type set passes N2.

## 11.10 What the further families add

Table 5 gives proposed decisions. Three lessons bear on the admission graph. First, the license is attached to the item or the version, not to the portal: figshare, CSIRO, arXiv and the city portals all vary it, so the N2 card check records the license field of the single item and of the single version. Second, a copy can outlive a change: arXiv keeps withdrawn versions available and NYC keeps no older versions, so the ledger saves the license text and the retrieval time. Third, personal data sits outside several licenses by their own terms, so the cleaning route (Table 4) is run before any admission.

| Source family | What the pages read say | Proposed decision |
|---|---|---|
| arXiv metadata and bulk full text | Metadata CC0; full text under a per-paper, per-version license; storing and serving barred unless the license permits; one request per three seconds for legacy interfaces [64][65][66][67][68] | Pick narrowly: metadata freely; full text only for papers whose license field reads CC BY or CC Zero, through the bulk route, with the version's license read |
| arXiv LaTeX source | Present only where submitted; may carry ancillary files; whether the paper's license covers source is not stated [69][66] | Hold: do not pick author comments; admit source only for CC BY or CC Zero papers after the license-coverage question is settled |
| figshare | CC0 is a dataset default, CC BY is also available; check the license per item; bulk use subject to the item's license; terms of service not read [71][72] | Pick narrowly: CC0 or CC BY items, item by item; hold items under repository-set terms |
| CSIRO Data Access Portal | Six Creative Commons options for data, older non-commercial licenses on some collections, a restricted tier needing an agreement; no bulk data route found [73][74][75][76] | Pick narrowly: collections under CC BY or CC BY-SA, license recorded per collection; hold NC and ND collections unless the use fits; do not touch the restricted tier |
| Toronto Open Data | Open Government Licence – Toronto, commercial use allowed with attribution; personal information excluded; one sample dataset marked Retired [82][83] | Pick narrowly: named, current datasets; skip retired ones; keep the attribution statement |
| NYC Open Data | No named open license; city website terms plus agency terms; check version history per dataset [77][78] | Hold: read each dataset's own license and agency terms first |
| Denver Open Data Catalog | Says users may copy, distribute and adapt; page content dates to 2018 [81] | Hold: read the current terms page before any pick |
| City of Chicago Data Portal | No license on the page read; disclaimer page unreadable [80] | Hold: unread terms are not admitted |

*Table 5.* Further families and proposed decisions (v0.5).

# 12. Running the author's receipt tools on this paper

Three of the author's published tools were run on this paper's own working files, and a fourth repository was re-run to check that its published result repeats: QuoteLedger 0.1.0, which checks each claim against the evidence label it carries; Fencekeeper 0.1.0, which inspects what still depends on a record before it is retired; EditAuditor 0.1.0, which compares a document with its revision; and the Free Evidence Benchmark, which runs the first three on constructed claims. Each was run from the author's local copy after the files matched their published checksums, offline, on this paper's own records and no other data; the two packaged programs were run in Python's isolated mode. None of the tools authorizes an action; each reports.

## 12.1 QuoteLedger on the claims table

Of the 65 claim rows, 59 carried a retrievable address and were run as declared leads; six had none (the not-found and unchecked rows). The audit found 59 declared claims, no exact-quotation claims, no primary-quote claims and no reviewed primary claims. The default policy was met, which the tool's own documentation says does not mean primary verification. Under the stricter policy that asks for a primary quotation, the policy was not met (exit 1). The plain reading is that every claim with a retrievable address (59 of 65 at that stage) is a lead read from a search extract or page summary, not a quotation checked against a page opened in full. That agrees with the provisional grades. A re-read of the decision rows at their pages, followed by a second run, is a planned test.

## 12.2 Fencekeeper on the paper's own versions

A packet of eight records described the paper's three versions, the archived copy of the first version, the private claims table, the gate report, the project copy of the delineation list and the intake note, with the dependencies between them, and asked for the first and second versions to be retired. The tool's answer was that review is required (exit 1). The first version has three current dependents (the archived copy, the claims table and the gate report), so it cannot be retired until each is dealt with. The second version has no current dependents but still needs a person's review. The relationships in the packet are the author's assertions, which the tool's documentation lists as a limit, and its report does not authorize any deletion.

## 12.3 EditAuditor on the paper's revisions

The archived first version and the current text were compared. The tool returned that review is needed (exit 1): 103 blocks preserved, 28 source blocks unaccounted for, 81 output blocks with no match in the source, and one finding not yet acknowledged. This is the expected shape for a revision that removed three groups of material, added three sections and renumbered the references. The tool cannot tell which of the 28 are the intended omissions and which are rewordings that need a person's eye, and those 28 have not yet been reviewed one by one. The report omits the text itself by default.

## 12.4 The benchmark repeated

The Free Evidence Benchmark's own tests (9) passed, and a fresh run of its held-out split gave 720 cases, 5,040 arm decisions and 200 full-workflow clearances, the figures its README states. The regenerated fixture and the run's output files match the known fingerprints in its verification file. The run used Python 3.10.12, not the 3.12.10 its README names as the verified environment, so the match shows that the result repeats on a second interpreter version, not that the environment is irrelevant. The benchmark scores constructed claims; it says nothing about real data and is not evidence for H1 to H4. Its separate recount step, which needs an isolated replay folder, was not run.

## 12.5 Re-run on draft v0.5

The same three tools were run on the v0.5 files. QuoteLedger read 76 claim rows that carry an address (the table now has 86 rows; five are marked omitted and five have no address). It found 76 declared claims, none an exact quotation, a primary quotation or a reviewed primary claim; the default policy was met and the strict policy was not (exit 1), as before. A first pass of this run read only 41 rows because the extraction of addresses dropped rows whose address sat in angle brackets; it was set aside and redone. Fencekeeper was given ten records and asked to retire the first four versions; it returned that review is required, kept the archived copy of the first version as a current dependent, quarantined versions one to four and retired nothing. EditAuditor compared v0.4 with v0.5 and returned that review is needed: 184 blocks preserved, 14 source blocks unaccounted for, 48 output blocks with no match, and two findings about changed heading context not yet acknowledged. The drafting handoff’s interpretation of the 14, made by comparing block text between the two files and counting list items as blocks, is that each is a block changed or withdrawn on purpose: the title and status lines, the introduction, three tables, two lists of limitations and readings, a withdrawn section, Section 11.6, the conclusion and the reference list. The tool's own review file was not written, so the tool still reports them as unaccounted. The benchmark was not rerun in that drafting pass. The public-edition replay is reported below.

## 12.6 Checks on the public edition

The original 76 address-bearing claims reproduced at the lead level. For this edition, six narrower assertions were checked separately against text retrieved from the publishers or maintainers. The checks cover the CC0 statement in CERN’s policy record [12], the portal’s focus on levels 2 and 3 [14], the publication year discussed by Duke for U.S. Public Domain Day 2026 [16], arXiv’s statement about who chooses the license [67], Toronto’s attribution requirement [82], and Czkawka’s description of duplicate matching [63]. QuoteLedger matched all six passages at their recorded character offsets. Those matches establish what those pages said when read. Each archive entry and each proposed use still needs its own rights and relevance decision.

EditAuditor reproduced the before-and-after counts in Section 12.5. Fencekeeper again retained the current dependent and retired zero records. The Free Evidence Benchmark was rerun on its held-out fictional fixture. Its nine unit tests passed. The fixture and decision outputs reproduced byte for byte, and a separate recount covered all 5,040 decisions across 720 cases and seven workflows. The workflow with recorded review cleared 200 cases, including 80 labelled unsupported by the fixture. The example shows why a recorded review can still be wrong. It supplies no performance estimate for the archives in this paper.

The four programs used were [QuoteLedger](https://github.com/OneiroNexus/QuoteLedger/releases/tag/v0.1.0), [EditAuditor](https://github.com/OneiroNexus/EditAuditor/releases/tag/v0.1.0), [Fencekeeper](https://github.com/OneiroNexus/Fencekeeper/releases/tag/v0.1.0), and [Free Evidence Benchmark](https://github.com/OneiroNexus/Free-Evidence-Benchmark/releases/tag/v0.1.0).

# 13. Residual risks and the gate that answers each

Table 6 sets each risk beside the step of the admission graph that is meant to answer it. These are design proposals and are untested; H2 to H4 are the tests that bear on them.

| Risk | Where it comes from | Answering step | What stays open |
|---|---|---|---|
| A few harmful records inside an otherwise clean pool | Section 4.1 | N3 probe, with a person reading the sample; per-record examination | The probe sees only what a person reads |
| A stated license is wrong or has drifted | Section 4.2 | N2 saves the license text as read, dated and fingerprinted; re-read on a schedule; takedown route recorded | A source can change between reads |
| Unmarked model-generated text | Section 4.3 | Provenance flag at N2; records of unknown provenance are retirement candidates | Marking depends on the source's own statements |
| Instructions hidden in data that a model may follow | Common to scraped text | N5 flags lines addressed to an agent and treats them as data | Reworded instructions can pass a simple check |
| A derivative that outlives its parent | Section 11.6 | The derivative carries upstream attribution and a ledger row that points to the parent; a takedown of the parent flags the derivative | Third parties holding copies |
| Two pages of one source disagree | NIST fee-based count, Section 11.2 | Both readings are kept in the ledger; neither is chosen by guess | Needs a person to settle it at the source |
| Personal data in a record | Any open archive | Count-only scan; matches are never stored | Shapes that the scan does not know |
| A license that differs by item or by version, or terms that could not be read | Sections 11.7 to 11.9 | N2 records the license field of the single item and version and saves the text; an unreadable terms page leaves the source on hold | Terms can change between reads |
| A tool's pass taken as proof | Section 12.1 | Tool results are labelled as leads or checks, never as verification of the data | Reviewer discipline |

*Table 6.* Residual risks and answering steps.

# 14. Conclusion

A data set is a set of decisions. The cheapest decision, to take what is reachable, is also the one that leaves the most to chance: records that carry another party's rights, records that are not what their card says, and a few that are worse. The sources checked support the narrow claim that per-record examination cannot be avoided by volume. The delineation sorts 17 entries into pick, hold, do not pick and retire, and the later tables add eight further candidates (Table 3) and seven further sources in four families (eight rows in Table 5). The admission graph gives every record the same path. What remains is to run the four tests.

# Declarations

**Contributions and editorial assistance.** Aaron Michael Weis conducted the research and directed the paper. Claude (Anthropic) assisted with drafting and source checks. Codex (OpenAI) prepared the public edition and reran the evidence tools.

**Competing interests.** The author owns Oneiron Holdings LLC. He developed the evidence tools evaluated in Section 12.

**Funding.** No external funding.

**Data and code availability.** The reference list identifies the public archives and studies discussed here. Source extracts and summaries informed the initial survey. Section 12.6 documents the scope of the follow-up checks. The four published tools are linked there. This paper distributes no dataset or new software.

**License and distribution.** This paper is released under CC BY 4.0 (https://creativecommons.org/licenses/by/4.0/). Share and adapt with credit to the author, a link to the license, and a note of any changes.

**Credit line.** Aaron Michael Weis (Oneironexus · Oneiron Holdings LLC · ORCID 0009-0002-1906-148X), 2026. "Choosing What to Collect". https://github.com/OneiroNexus/choosing-what-to-collect

# References

1. Souly A, et al. Poisoning Attacks on LLMs Require a Near-constant Number of Poison Samples. arXiv:2510.07192. <https://arxiv.org/abs/2510.07192>
2. Anthropic, UK AI Security Institute, Alan Turing Institute. A small number of samples can poison LLMs of any size. <https://www.anthropic.com/research/small-samples-poison>
3. Longpre S, Mahari R, Chen A, et al. A large-scale audit of dataset licensing and attribution in AI. Nature Machine Intelligence 6:975–987 (2024). <https://doi.org/10.1038/s42256-024-00878-8>; preprint arXiv:2310.16787.
4. Shumailov I, Shumaylov Z, Zhao Y, Papernot N, Anderson R, Gal Y. AI models collapse when trained on recursively generated data. Nature 631:755–759 (2024). <https://doi.org/10.1038/s41586-024-07566-y>
5. Author Correction: AI models collapse when trained on recursively generated data. Nature (2025). <https://doi.org/10.1038/s41586-025-08905-3>
6. Borji A. A Note on Shumailov et al. (2024). arXiv:2410.12954.
7. Common Crawl. About. <https://blog.commoncrawl.org/about>
8. Baack S. Training Data for the Price of a Sandwich: Common Crawl's Impact on Generative AI. Mozilla Foundation, 2024. <https://www.mozillafoundation.org/en/research/library/generative-ai-training-data/common-crawl/>
9. NASA Earthdata. Data use policy; Open science. <https://www.earthdata.nasa.gov/learn/use-data/data-use-policy>; <https://www.earthdata.nasa.gov/about/open-science>
10. Willett DS, et al. NOAA Open Data Dissemination: Petabyte-scale Earth system data in the cloud. Science Advances (2023). <https://repository.library.noaa.gov/view/noaa/59059>
11. AWS Marketplace listing, NOAA Atmospheric Climate Data Records (license statement; secondary host). <https://aws.amazon.com/marketplace/pp/prodview-mmz4ve4u5cdui>
12. CERN Open Data Policy for the LHC Experiments, record 416 (CC0). <https://opendata.cern.ch/record/416>
13. CERN Open Data portal: Ten years of CERN Open Data portal (2024). <https://opendata.cern.ch/docs/ten-years-of-cern-open-data-portal>
14. CERN Open Data portal: About (data levels). <https://opendata.cern.ch/docs/about>
15. Library of Congress. HABS/HAER/HALS rights and restrictions. <https://www.loc.gov/item/az0213> and <https://www.loc.gov/rr/print/res/114_habs.html>
16. Jenkins J, Boyle J. Public Domain Day 2026. Duke Center for the Study of the Public Domain. <https://web.law.duke.edu/cspd/publicdomainday/2026/>
17. HathiTrust. Acceptable Use Policy. <https://hathitrust.org/acceptable-use>
18. Internet Archive. Rights (help pages). <https://help.archive.org/help/rights/>
19. Zacchiroli S, et al. Software Heritage topology study (EMSE, 2026). <https://upsilon.cc/~zack/research/publications/emse-2026-swh-topology.pdf>
20. Software Heritage. Terms of use for bulk access. <https://www.softwareheritage.org/legal/bulk-access-terms-of-use/>
21. NASA STI. Disclaimers. <https://sti.nasa.gov/disclaimers/>
22. Federation of American Scientists. NTRS taken offline (2013). <https://fas.org/?p=11564>
23. Lebofsky M, et al. The Breakthrough Listen Search for Intelligent Life: Public Data, Formats, Reduction and Archiving. arXiv:1906.07391.
24. Breakthrough Initiatives. Open Data Archive. <https://breakthroughinitiatives.org/opendatasearch>
25. IETF. Guidelines to Authors of Internet-Drafts. <https://www.ietf.org/ietf-ftp/ietf/1id-guidelines.html>
26. Carpenter B. Process Document Anachronisms (Internet-Draft, 2026). <https://datatracker.ietf.org/doc/draft-carpenter-gendispatch-anachronisms/>
27. openFDA. Device 510(k) overview. <https://open.fda.gov/apis/device/510k>
28. openFDA. Download API fields (disclaimer). <https://open.fda.gov/apis/download-api-fields/>
29. arXiv. Reuse requests. <https://info.arxiv.org/help/license/reuse.html>
30. arXiv. Terms of use for arXiv APIs. <https://info.arxiv.org/help/api/tou.html>
31. arXiv. Bulk data access, Amazon S3. <https://info.arxiv.org/help/bulk_data_s3.html>
32. NC State University Libraries. arXiv bulk data access (secondary). <https://www.lib.ncsu.edu/node/42245>
33. GrabCAD Help. How can models be used and shared? <https://help.grabcad.com/article/246-how-can-models-be-used-and-shared>
34. All3DP. Weekend poll (April 2026), Thingiverse license types (secondary). <https://all3dp.com/6/do-you-upload-models-to-3d-printing-repositories-or-just-download/>
35. Techdirt. Seven years ago, CERN gave open access a huge boost; now it's doing the same for open data (secondary report of the CERN policy, 2021). <https://www.techdirt.com/2021/01/04/seven-years-ago-cern-gave-open-access-huge-boost-now-doing-same-open-data/>
36. CERN Open Data portal, news and updates list (2024 items). <https://opendata.web.cern.ch>
37. Toffolin L, et al. ATLAS Open Data conference paper (LHCP 2025, INSPIRE record). <https://inspirehep.net/files/1cb109da43d8028c9de10311bacde21c>
38. CERN Open Data portal, home page news (2025 to 2026 items). <https://opendata.cern.ch/>
39. Library of Congress. Chronicling America, technical information (bulk OCR). <https://www.loc.gov/collections/chronicling-america/about-this-collection/technical-information/>
40. Library of Congress NDNP. Site visit data and API slides (April 2026). <https://loc.gov/ndnp/guidelines/docs/GASiteVisitDataAPI20260401.pdf>
41. Dell M, et al. American Stories: A Large-Scale Structured Text Dataset of Historical U.S. Newspapers. arXiv:2308.12477.
42. Newswire: A Large-Scale Structured Database of a Century of Historical News. arXiv:2406.09490.
43. Smithsonian Open Access, welcome page. <https://www.si.edu/node/631369>
44. Smithsonian Open Access, 21st century diffusion (3D models). <https://dashboard.si.edu/openaccess/updates/21st-century-diffusion>
45. Smithsonian news release, 25 February 2020. <https://www.si.edu/newsdesk/releases/smithsonian-releases-28-million-free-images-broader-public-use>
46. Smithsonian Libraries and Archives. Biodiversity Heritage Library Open Data Collection (Figshare). <https://smithsonian.figshare.com/projects/Biodiversity_Heritage_Library_Open_Data_Collection/151911>
47. Crystallography Open Database. <https://www.crystallography.net/cod>
48. Crystallography Open Database mirror page (secondary). <https://qiserver.ugr.es/cod/>
49. Data.gov record, Planetary Data System. <https://catalog.data.gov/dataset/planetary-data-system-pds>
50. NASA. Data by subject (PDS nodes). <https://www.nasa.gov/nasa-data-by-subject>
51. NIST. Standard Reference Data. <https://www.nist.gov/srd>
52. NIST. Standard reference data feature (copyright statement). <https://www.nist.gov/node/1702106>
53. Data.gov record, NIST Chemistry WebBook SRD 69. <https://catalog.data.gov/dataset/nist-chemistry-webbook-srd-69>
54. EarthScope. Data and software (SAGE facility). <https://www.iris.edu/hq/data_and_software>
55. EarthScope. Sponsored open data. <https://docs.earthscope.org/sponsored-open-data>
56. NSF SAGE Data Management Center. Restricted Data Access. <https://ds.iris.edu/ds/nodes/dmc/data/types/restricted/>
57. OpenRefine. Privacy. <https://openrefine.org/privacy>
58. OpenRefine with a local model (Dataharvest 2026 slides). <https://hosted-files.sched.co/dataharvest26/e3/refine-llm-en.pdf>
59. Presidio. Official documentation for text and image de-identification. <https://presidio.dataprivacystack.org/>
60. Presidio maintainers. Presidio project repository. <https://github.com/data-privacy-stack/presidio>
61. Gitleaks maintainers. Gitleaks project repository. <https://github.com/gitleaks/gitleaks>
62. Truffle Security. TruffleHog project repository. <https://github.com/trufflesecurity/trufflehog>
63. Czkawka maintainers. Czkawka project repository. <https://github.com/qarmin/czkawka>
64. arXiv. Bulk data access. <https://info.arxiv.org/help/bulk_data.html>
65. arXiv. Bulk data access through Amazon S3. <https://info.arxiv.org/help/bulk_data_s3.html>
66. arXiv. API terms of use. <https://info.arxiv.org/help/api/tou.html>
67. arXiv. Licenses. <https://info.arxiv.org/help/license/index.html>
68. arXiv. Licenses: reuse of e-prints. <https://info.arxiv.org/help/license/reuse.html>
69. arXiv. Submitting TeX/LaTeX; ancillary files. <https://info.arxiv.org/help/submit_tex.html>; <https://info.arxiv.org/help/ancillary_files.html>
70. arXiv. Withdrawing a paper. <https://info.arxiv.org/help/withdraw.html>
71. figshare. Policies. <https://info.figshare.com/user-guide/figshare-policies/>
72. figshare. API documentation. <https://docs.figshare.com/>
73. CSIRO Data Access Portal. Collection development plan. <https://research.csiro.au/dap/about/collection-development-plan>
74. CSIRO Data Access Portal. Licences. <https://research.csiro.au/dap/licences>
75. CSIRO Data Access Portal. Licence deed for specimen images with restricted access. <https://research.csiro.au/dap/licences/csiro-copyright-licence-deed-for-specimen-images-with-restricted-access>
76. CSIRO Data Access Portal. Harvesting metadata. <https://research.csiro.au/dap/developer-tools/harvesting-metadata>
77. NYC Open Data. Overview. <https://opendata.cityofnewyork.us/overview/>
78. City of New York. NYC Open Data Terms of Use. <https://data.cityofnewyork.us/stories/s/Terms-of-Use/k9k7-3cje>
79. Socrata. Application tokens (vendor documentation). <https://dev.socrata.com/docs/app-tokens.html>
80. City of Chicago. About the data portal. <https://chicago.gov/city/en/narr/foia/CityData.html>
81. City and County of Denver. Open data catalog. <https://www.denvergov.org/opendata>
82. City of Toronto. Open Government Licence – Toronto. <https://open.toronto.ca/open-data-licence/>
83. City of Toronto. Street tree data (marked Retired). <https://open.toronto.ca/dataset/street-tree-data/>
84. NYC Open Data. 311 service requests dataset page (title only). <https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9>
85. City of Chicago. Building permits dataset page (title only). <https://data.cityofchicago.org/Buildings/Building-Permits/ydr8-5enu>
