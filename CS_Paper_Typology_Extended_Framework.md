# Extended Framework for Paper Typology in Computer Science
## Contribution Novelty Gradients, Hybrid Contributions, and Strategic Type Selection

**Prepared by:** Research Methodology Analysis  
**Audience:** PhD Researchers, Postdoctoral Scientists, Senior Practitioners  
**Status:** Reference Document — Extended Edition

---

## Table of Contents

1. [Overview and Motivation](#1-overview-and-motivation)
2. [Canonical Paper Type Taxonomy (Revised)](#2-canonical-paper-type-taxonomy-revised)
3. [Contribution Novelty Gradients](#3-contribution-novelty-gradients)
   - 3.1 [Defining Novelty as a Multidimensional Construct](#31-defining-novelty-as-a-multidimensional-construct)
   - 3.2 [The Novelty–Validation Obligation Curve](#32-the-noveltyvalidation-obligation-curve)
   - 3.3 [Novelty Gradient by Paper Type](#33-novelty-gradient-by-paper-type)
4. [Hybrid Contributions: Taxonomy and Resolution Strategies](#4-hybrid-contributions-taxonomy-and-resolution-strategies)
   - 4.1 [Why Hybrids Arise and Why They Fail](#41-why-hybrids-arise-and-why-they-fail)
   - 4.2 [Canonical Hybrid Configurations](#42-canonical-hybrid-configurations)
   - 4.3 [Decomposition Strategies for Hybrid Work](#43-decomposition-strategies-for-hybrid-work)
5. [Model–Type–Novelty Alignment Matrix](#5-modeltypenovelty-alignment-matrix)
6. [Venue Selection as a Function of Novelty and Type](#6-venue-selection-as-a-function-of-novelty-and-type)
7. [Decision Protocol for Researchers](#7-decision-protocol-for-researchers)
8. [Common Failure Modes and Corrective Actions](#8-common-failure-modes-and-corrective-actions)
9. [Worked Examples](#9-worked-examples)
10. [Conclusions](#10-conclusions)
11. [References](#11-references)

---

## 1. Overview and Motivation

The original taxonomy established that paper types in computer science encode intent — signaling to reviewers the nature of a contribution, the expected level of validation, and the appropriate modeling strategy. A central finding was that many rejections arise not from weak ideas but from misalignment between paper type, model type, and validation approach (Wieringa, 2014).

This extended report addresses two questions left open by that analysis:

**First**, how does the *degree* of novelty in a contribution interact with paper type selection? Not all full research papers propose equally disruptive claims, and not all idea papers are equally speculative. The relationship between novelty and validation obligation is non-linear and context-dependent in ways that the original taxonomy did not capture.

**Second**, how should a researcher handle a contribution that is genuinely hybrid — one that simultaneously constitutes, for example, a system artifact and a methodological advance, or an empirical study and a conceptual framework? Hybrid contributions are common in mature subdisciplines but are routinely mishandled, leading to papers that satisfy neither reviewers evaluating the system nor those evaluating the methodology.

The extended framework presented here integrates the novelty gradient concept into the existing taxonomy, provides a principled typology of hybrid configurations, and offers a decision protocol that researchers can apply directly at the point of paper framing.

---

## 2. Canonical Paper Type Taxonomy (Revised)

The table below reproduces and refines the original taxonomy. Columns for Novelty Tier and Hybrid Potential have been added; the Validation Expectation column has been made more precise for types where the original was insufficiently specific. Dataset contribution papers have been added as a canonical type (Gebru et al., 2021; Paullada et al., 2021). Survey and systematic literature review have been separated (Kitchenham et al., 2009).

| Paper Type | Core Purpose | Typical Contribution | Validation Expectation | Model Type | Novelty Tier | Hybrid Potential |
|---|---|---|---|---|---|---|
| **Idea Paper** | Introduce a novel concept early | New hypothesis, framing, or conjecture | Plausibility, motivation, absence of obvious refutation | Conceptual model, thought experiments | Disruptive–Incremental | Low |
| **Position Paper** | Argue a stance or vision for a field | Grounded opinionated argument | Logical coherence, citation coverage, acknowledgment of counterarguments | Argumentative / conceptual model | Disruptive–Incremental | Low |
| **Short Paper** | Report partial or narrowly scoped results | Early result or focused insight | Light empirical or analytical validation; scope explicitly bounded | Simplified system or analytical model | Incremental | Moderate |
| **Full Research Paper** | Advance state of the art | Algorithm, theory, system, or method | Strong empirical, formal, or theoretical validation; threats-to-validity addressed | Formal, mathematical, or system model | Disruptive–Incremental | High |
| **Conceptual Paper** | Structure or reconceptualize a problem space | Taxonomy, ontology, framework, or reframing | Internal consistency, literature coverage, discriminative power of categories | Conceptual framework / meta-model | Reconceptualizing | Moderate |
| **Survey** | Synthesize and organize existing work | Structured comparison, classification scheme | Coverage completeness, classification rigor, currency | Taxonomy or classification model | Low–None | Low |
| **Systematic Literature Review (SLR)** | Answer a specific research question via reproducible protocol | Protocol-driven evidence synthesis | Protocol pre-registration, inclusion/exclusion criteria, inter-rater reliability, compliance with established SLR guidelines (e.g., Kitchenham et al., 2009) and reporting standards (e.g., PRISMA) | Evidence synthesis model | Low–None | Low |
| **System Paper** | Describe a significant built artifact | Architecture, design decisions, lessons learned | System evaluation on representative benchmarks; deployment evidence preferred | Architecture model, pipeline diagrams | Incremental–Disruptive | High |
| **Methodology Paper** | Propose a new research or engineering method | Process, technique, or workflow | Demonstration on representative cases; comparison to alternatives | Process or workflow model | Incremental–Disruptive | High |
| **Empirical Study** | Observe and characterize real-world behavior | Measurements, datasets, statistical models, causal inference | Statistical rigor; effect sizes; threats to validity (construct, internal, external, conclusion); pre-registration where applicable | Statistical or experimental model | Low–Incremental | Moderate |
| **Dataset Contribution** | Create and document a resource enabling future research | Curated dataset with datasheet | Data collection methodology, representativeness, bias analysis, datasheet documentation, licensing | Data model; documentation schema | Incremental | Moderate |
| **Industrial / Experience Paper** | Share practitioner insights grounded in deployment | Lessons, failure analyses, contextual constraints | Ecological validity, credibility through detail; generalizability bounded honestly | Reference architecture, decision models | Low–Incremental | Moderate |
| **Vision Paper** | Articulate a long-term research roadmap | Open problems, research directions, sociotechnical framing | Accurate characterization of current state; coherent trajectory; domain expertise evident | High-level conceptual model | Disruptive | Low |
| **Negative Results Paper** | Report informative non-results | Refutation of a plausible hypothesis; design space elimination | Sound methodology; sufficient statistical power; genuine plausibility of refuted hypothesis | Experimental model | Incremental–None | Low |
| **Replication Paper** | Test robustness of prior claims | Confirmation or qualified refutation | Methodological rigor; explicit replication type (exact vs. conceptual); variance reporting | Original model (exact) or operationally varied model (conceptual) | None | Low |
| **Tool / Demo Paper** | Present a usable artifact | Practical software or hardware tool | Usability; deployment evidence or user study; artifact availability | Software architecture model | Incremental | Low |

---

## 3. Contribution Novelty Gradients

### 3.1 Defining Novelty as a Multidimensional Construct

Novelty is frequently treated as a binary property in informal discourse — a contribution is either novel or it is not. This is analytically inadequate. Gregor and Hevner (2013), working in the design science tradition, proposed a knowledge contribution framework that positions research along dimensions of application domain maturity and solution maturity, with novelty as a distinguishing characteristic of the highest-impact contributions. Independently, Shull et al. (2008) provided methodological guidance for empirical software engineering research, including principles for characterizing the nature and scope of empirical contributions. Drawing on both traditions, novelty is better understood as operating across at least four independent dimensions:

**Conceptual novelty** refers to whether a new idea, abstraction, or theoretical construct is introduced. A paper that proposes a new model of distributed consistency is conceptually novel even if it produces no implementation.

**Technical novelty** refers to the introduction of a new algorithmic, architectural, or engineering approach. A paper may be technically novel without being conceptually novel — for instance, a new implementation of a known algorithm that achieves better asymptotic performance.

**Empirical novelty** refers to the production of new evidence about an understudied phenomenon, population, or context. A replication study of an existing result in a new ecological setting is empirically novel without being conceptually or technically novel.

**Application novelty** refers to the first principled application of an established technique or framework to a new problem domain. Transfer of a known method to a new domain — if the transfer is non-trivial — constitutes application novelty.

A contribution may be simultaneously novel along multiple dimensions (the strongest case for a full research paper), along only one dimension (typically justifying a short paper or focused venue), or along none (justifying a replication or experience paper). Reviewers implicitly evaluate novelty along these dimensions; making the novelty claim explicit in the introduction is a practical writing recommendation that directly reduces the rate of desk rejection.

### 3.2 The Novelty–Validation Obligation Curve

A critical structural relationship, not made explicit in the original taxonomy, is that the validation obligation of a paper scales monotonically with its novelty claims. This relationship can be stated as a principle:

> **The Validation Proportionality Principle:** The stronger and more specific a novelty claim, the more rigorous and targeted must be the evidence marshaled in support of it.

This is not merely normative; it reflects the epistemic logic of peer review. A claim of conceptual novelty requires the author to demonstrate that the proposed construct is not subsumed by existing ones — this is a literature-grounding obligation, not an experimental one. A claim of technical novelty requires the demonstration of correctness (formal proof, exhaustive testing, or both) and often of superiority over prior work. A claim of empirical novelty requires that the measurement is sound, the phenomenon is real, and the threat to validity analysis is credible.

The practical implication is that a paper making modest novelty claims is not deficient — it is appropriately scoped. Problems arise when novelty claims and validation evidence are mismatched in either direction: overclaiming (strong novelty assertion with weak evidence) leads to rejection; underclaiming (strong evidence with timid framing) leads to acceptance of a paper that could have had greater impact.

The following figure describes this relationship schematically.

```
Validation Rigor Required
        ▲
        │                                         ●  Full Research Paper
        │                                    ●  Methodology Paper
        │                              ●  System Paper
        │                         ●  Empirical Study
        │                    ●  Short Paper
        │               ●  Dataset Contribution
        │          ●  Conceptual Paper
        │     ●  Idea Paper / Position Paper
        │ ●  Survey / SLR / Replication / Experience
        └────────────────────────────────────────────► Novelty Claimed
           Low                                    High
```

*Figure 1. Schematic representation of the Validation Proportionality Principle. Position along both axes reflects expected norms, not rigid prescriptions.*

### 3.3 Novelty Gradient by Paper Type

The following elaborates the novelty tier assigned in Table 1 with the specific novelty dimensions relevant to each type.

**Disruptive novelty** is appropriate for vision papers, idea papers, and — when warranted — full research papers proposing fundamental reconceptualizations. Disruptive novelty implies claims that, if correct, invalidate or substantially supersede a significant body of prior work. The validation obligation at this tier is asymmetric: because the claim is strong, reviewers will require correspondingly strong disconfirmatory evidence to be addressed (i.e., why does the proposed framing not reduce to an existing one?).

**Incremental novelty** characterizes the majority of full research papers, system papers, methodology papers, and short papers. The contribution improves upon, extends, or applies existing knowledge in a meaningful but bounded way. Validation must demonstrate superiority over or complementarity with the closest prior work.

**Reconceptualizing novelty** is the defining characteristic of conceptual papers. The contribution does not propose new facts or artifacts but offers a new organizational or interpretive lens. The canonical example is Parnas (1972), which did not propose new algorithms but reframed the criterion for system decomposition in a way that was both discriminative and practically consequential. Similarly, Dijkstra (1968) — now a canonical example of a position paper with reconceptualizing impact — did not introduce a new programming construct but argued that unrestricted use of go to statements was harmful to program structure, fundamentally influencing the shift toward structured programming. Validation requires showing that the new conceptualization has greater explanatory or predictive power than its predecessors.

**Application novelty** characterizes many industrial papers, experience reports, and dataset contributions. The novelty lies in the application context, not in the method or theory. Validation must demonstrate that the application was non-trivial — that the transfer required adaptation, revealed new challenges, or produced insights that generalize back to the source domain.

**Zero novelty** is appropriate for replication papers, surveys, and SLRs. These paper types derive their value not from novelty but from epistemic functions: verification, synthesis, and consolidation. Framing such papers as novel is a category error that consistently leads to rejection. Negative results papers, though sometimes classified as having incremental novelty when they eliminate a portion of the design space, similarly derive their primary value from epistemic functions — specifically, correcting the publication record. The well-documented bias toward positive results across the sciences (Fanelli, 2010) makes such contributions structurally important even when they claim no novelty in the conventional sense.

---

## 4. Hybrid Contributions: Taxonomy and Resolution Strategies

### 4.1 Why Hybrids Arise and Why They Fail

Hybrid contributions arise naturally from the practice of research. A researcher who builds a system to test a theoretical claim has produced both a system artifact and theoretical evidence. A researcher who conducts an empirical study that also requires developing a new measurement instrument has produced both empirical findings and a methodological contribution.

The problem is not that hybrid contributions exist but that they are routinely submitted without acknowledging the hybrid structure — and without satisfying the validation requirements of either constituent type. A paper submitted as a system paper that also makes theoretical claims will be evaluated by system paper reviewers who are not equipped to validate the theory, and by theory reviewers who are unsatisfied by the system evaluation. The result is rejection on both grounds despite the paper potentially being meritorious on each.

There are two failure modes. The first is *contribution diffusion*: the paper attempts to make contributions on multiple fronts but allocates insufficient space and evidence to any one of them. The second is *type mislabeling*: the paper is submitted under a type that matches one of its constituent contributions but not the other, generating reviewer confusion about what is actually being claimed.

### 4.2 Canonical Hybrid Configurations

Research practice produces a relatively small number of recurring hybrid configurations. Each has a characteristic structure and a preferred resolution strategy.

---

**Configuration 1: System + Methodology**

*Structure:* The paper builds a non-trivial system and, in doing so, proposes a new engineering or research method. The system is both the artifact and the proof-of-concept for the method.

*Example context:* A paper that builds a novel static analysis framework and also articulates a new methodology for extending it to new language families.

*Failure mode:* System reviewers accept the system evaluation but reject the methodology as insufficiently demonstrated. Methodology reviewers accept the process model but find the system evaluation insufficient as a demonstration case.

*Resolution:* Separate the contributions into two papers if both are mature. If they must be unified, foreground one contribution as primary and demote the other to a "secondary contribution" or "enabling artifact." The validation section must address both — system benchmarks for the artifact, and at least one additional case study or comparative analysis for the methodology.

---

**Configuration 2: Empirical Study + Conceptual Framework**

*Structure:* The paper conducts an empirical study (e.g., a large-scale measurement study or controlled experiment) and, on the basis of findings, proposes a new conceptual framework or taxonomy that explains the results.

*Example context:* A study of developer behavior in code review that both reports statistical findings and proposes a cognitive load taxonomy to explain observed patterns.

*Failure mode:* Empirical reviewers evaluate the statistical methodology rigorously but find the taxonomy underdeveloped or unfalsifiable. Conceptual reviewers find the framework interesting but feel it is not sufficiently evaluated as a standalone conceptual contribution.

*Resolution:* This configuration is most naturally handled as a full research paper in which the empirical study is the primary contribution and the framework is presented as a derived artifact — a theoretical account that organizes the findings. The framework's validation is then implicit in the quality of the empirical grounding. If the framework is intended as a standalone contribution, it should be published separately, citing the empirical paper as supporting evidence.

---

**Configuration 3: System + Empirical Study**

*Structure:* The paper builds a system and then uses the system to conduct an empirical study of a real-world phenomenon that the system uniquely enables.

*Example context:* A paper that builds a dynamic analysis tool for mobile applications and uses it to characterize energy consumption patterns across a corpus of production apps.

*Failure mode:* The paper is treated as a system paper, but reviewers find the evaluation is really a study — the system is only a means, not the end. Alternatively, it is treated as an empirical study, but reviewers question the generalizability of findings that depend on a single bespoke tool.

*Resolution:* If the system is non-trivial and the study is large-scale and independently significant, this warrants two papers — a system paper and an empirical paper. If the system is primarily an enabling artifact, the paper should be framed as an empirical study with the system described as an infrastructure contribution in a self-contained methods section. The key signal is whether a reader of the system section alone would find it publishable — if not, it is an enabling artifact, not a co-equal contribution.

---

**Configuration 4: Methodology + Empirical Validation**

*Structure:* The paper proposes a new research or engineering methodology and validates it empirically, often via a controlled experiment or comparative case study.

*Example context:* A paper proposing a new mutation testing strategy for concurrent programs, evaluated empirically against existing strategies on a benchmark suite.

*Failure mode:* The methodology description is insufficiently formal (lacking a process model or decision criteria), so reviewers treat the paper as purely empirical and find the methodology claim unjustified. Alternatively, the empirical evaluation is too narrow to justify the breadth of the methodology claim.

*Resolution:* Explicitly structure the paper with a methodology section (process model, decision criteria, applicability conditions) followed by a separate evaluation section (experimental design, threats to validity, results). The methodology section should be self-contained enough that a reader could apply the method without the paper's specific evaluation context. Framing in the introduction must state clearly that both are being claimed.

---

**Configuration 5: Vision + Evidence**

*Structure:* The paper articulates a long-term research vision but grounds it in preliminary empirical or system evidence rather than relying purely on argumentation.

*Example context:* A vision paper for a new paradigm of human-AI collaborative programming, supported by a small-scale user study demonstrating initial feasibility.

*Failure mode:* Vision paper reviewers find the empirical section distracting and insufficiently rigorous. Empirical reviewers find the study too small to publish on its own.

*Resolution:* This is one of the few hybrid configurations where unification is strongly preferred. The evidence serves a rhetorical function (grounding plausibility) rather than a full evidentiary one; it should be presented as such, with explicit caveats on scope. The paper should be framed as a vision paper with supporting preliminary evidence, not as an empirical paper with visionary implications.

---

### 4.3 Decomposition Strategies for Hybrid Work

When a hybrid contribution is sufficiently mature on both fronts to warrant separate publication, decomposition is the recommended strategy. The following principles govern ethical and strategic decomposition.

**Independence principle:** Each decomposed paper must make a self-contained contribution that can be evaluated without reference to the other. Cross-referencing is permitted and encouraged, but each paper must stand alone under peer review.

**Non-redundancy principle:** The two papers must not re-publish the same content. Shared background or methods sections must be differentiated sufficiently that neither paper could be accused of self-plagiarism. In practice, the shared content should be cited, not reproduced.

**Sequencing principle:** When papers are causally dependent (Paper B uses the system built in Paper A), submit Paper A first. Do not submit both simultaneously to different venues without disclosing this in both cover letters, as this can create conflicts during the review process if the same reviewer is assigned to both.

**Disclosure principle:** Acknowledge the companion paper in the submission, using a note such as "a related contribution describing the system infrastructure is under concurrent submission at [venue]." Most program committees consider this acceptable; concealment can be grounds for rejection upon discovery.

---

## 5. Model–Type–Novelty Alignment Matrix

The following matrix extends the original model-type heuristic by incorporating the novelty dimension. Each cell prescribes the modeling approach most appropriate for a given combination of paper type and novelty tier.

| Paper Type | Disruptive Novelty | Incremental Novelty | Application / Reconceptualizing | Zero Novelty |
|---|---|---|---|---|
| **Full Research Paper** | Formal model + existence proof + comparative evaluation | Formal or system model + ablation study + benchmark comparison | System or process model + transfer analysis + domain-specific evaluation | Not applicable |
| **System Paper** | Architecture model + novel design rationale + end-to-end evaluation | Architecture model + component evaluation + comparison to nearest alternative | Architecture model showing adaptation decisions + deployment evidence | Not applicable |
| **Methodology Paper** | Process model + theoretical grounding + multiple case demonstrations | Process model + comparative demonstration on representative cases | Process model with adaptation guide + at least one full case study | Not applicable |
| **Empirical Study** | Experimental model + pre-registered hypotheses + large-scale evidence | Experimental model + threats-to-validity + effect sizes | Statistical model + contextual validity argument + replication invitation | Replication paper only |
| **Conceptual Paper** | Meta-model + comparative analysis against existing frameworks + discriminative power demonstration | Conceptual framework + literature mapping + practical applicability | Adapted framework + boundary conditions + domain validation | Not applicable |
| **Idea / Position / Vision** | Conceptual model + strong argumentation + preliminary feasibility signal | Conceptual model + literature grounding + scoped claims | Not typical | Not applicable |
| **Survey / SLR** | Not applicable | Not applicable | Classification model + coverage analysis | Protocol-driven evidence model (SLR) or structured classification (survey) |
| **Dataset Contribution** | Not typical | Data model + datasheet + bias analysis + baseline results | Data model + domain adaptation documentation + usage guidelines | Not applicable |
| **Replication / Negative Results** | Not applicable | Not applicable | Not applicable | Original experimental model (replication) or experimental model + power analysis (negative results) |

---

## 6. Venue Selection as a Function of Novelty and Type

Venue selection is downstream of paper type and novelty tier, but the relationship is not deterministic — multiple venue categories can be appropriate for a given combination, and the choice among them depends on intended audience and contribution emphasis.

The following generalizations hold across the major computing research communities.

**Top-tier conference venues** (e.g., SOSP, OSDI, PLDI, ICSE, NeurIPS, CVPR, STOC) expect full research papers or system papers with either disruptive or strong incremental novelty. The bar for empirical rigor at these venues has risen substantially over the past decade; papers lacking effect sizes, threats-to-validity sections, or artifact availability are increasingly desk-rejected at venues that have adopted artifact evaluation programs (ACM Artifact Review and Badging, 2020).

**Workshop venues** are appropriate for idea papers, position papers, short papers, and early-stage hybrid contributions. Submitting a mature, fully validated full research paper to a workshop represents a strategic error unless the venue has proceedings indexed in major databases and the author has a specific community-building rationale.

**Journal venues** (e.g., TOSEM, TSE, EMSE, JACM, TOCS) are appropriate for full research papers, SLRs, empirical studies, and replication papers. Journals offer the page budget required to fully document methodology, which makes them structurally better suited to SLRs and large-scale empirical studies than conferences. A paper requiring 30 pages to present its validation adequately should not be compressed into 12 conference pages — compression at that scale destroys the information a reviewer needs to evaluate the claim.

**Experience and industry tracks** at conferences (e.g., ICSE SEIP, FSE Industry) are appropriate for industrial/experience papers, tool papers, and dataset contributions with strong practitioner relevance. These tracks evaluate ecological validity and deployment scale as primary criteria, not conceptual or technical novelty.

**Dataset and benchmark tracks** (e.g., NeurIPS Datasets and Benchmarks) provide dedicated review criteria for dataset contributions. Other top-tier venues such as CVPR accept dataset and benchmark papers through their main research track rather than a separate submission track. Submitting a dataset paper to a main research track at a venue that lacks dedicated dataset review criteria risks evaluation against the novelty bar for full research papers, which is a systematic strategic error.

---

## 7. Decision Protocol for Researchers

The following decision protocol integrates the original taxonomy's self-assessment questions with the novelty gradient and hybrid contribution analysis developed above. Apply it sequentially at the point of paper framing, before writing begins.

---

**Step 1: Characterize your contribution along novelty dimensions.**

For each of the four novelty dimensions — conceptual, technical, empirical, application — ask: does my work introduce something genuinely new along this dimension, or does it reproduce, extend, or apply existing work? Assign each dimension a tier: disruptive, incremental, application/reconceptualizing, or zero. If all four dimensions are zero, the appropriate paper type is replication, survey, or experience report.

---

**Step 2: Identify the primary value created.**

Determine which single dimension of novelty is strongest. This is your primary contribution. The paper type is selected primarily to serve this contribution. Secondary contributions exist to strengthen the primary claim, not to constitute independent claims of equal weight.

---

**Step 3: Check for hybrid structure.**

If you have identified strong novelty along two or more independent dimensions — for example, a new system architecture (technical) and a new measurement methodology (methodological) — you have a hybrid contribution. Apply the decomposition analysis from Section 4.3: are both contributions sufficiently mature for independent publication? If yes, plan for two papers and apply the independence, non-redundancy, sequencing, and disclosure principles. If no, select the more mature contribution as primary and treat the other as a supporting artifact.

---

**Step 4: Determine the appropriate model type.**

Using the alignment matrix in Section 5, identify the model type appropriate for your paper type and novelty tier. If the model you currently have does not match — for instance, you have a system architecture model but you are claiming disruptive conceptual novelty — you have a framing problem, not a contribution problem. Either develop the appropriate model or revise the novelty claim.

---

**Step 5: Verify validation realism.**

Given your paper type, novelty tier, and model type, enumerate the validation elements that reviewers at your target venue will expect. For each element, assess whether you have the evidence now or a credible plan to obtain it before submission. If more than one critical validation element is absent, the contribution is not yet mature for submission. Submit to a workshop as an idea or position paper and revisit after collecting the missing evidence.

---

**Step 6: Select the venue.**

With paper type, novelty tier, and validation realism established, select the venue category (Section 6) and then the specific venue based on scope alignment and community fit. Do not allow venue prestige to drive paper type selection — submitting to a top-tier conference a contribution that is structurally a workshop paper wastes reviewer time and damages the author's relationship with that program committee.

---

## 8. Common Failure Modes and Corrective Actions

The following failure modes are among the most frequently observed at program committees and represent systematic, correctable errors rather than idiosyncratic ones.

**Novelty overclaiming.** The introduction frames a contribution as disruptive when the evidence supports only incremental novelty. Reviewers interpret this as either naivety or misleading framing; either assessment leads to rejection. *Corrective action:* Audit every novelty claim in the introduction and abstract against the evidence in the evaluation section. Every claim of novelty must be directly falsifiable by a specific result or comparison.

**Validation underfitting.** The validation is appropriate for a lower novelty tier than the contribution claims. An idea paper's validation presented in a full research paper context signals that the authors do not understand peer review norms. *Corrective action:* Re-read the calls for papers of your target venue for explicit statements of required validation. If the call does not specify, examine the last two years of accepted papers in the same category.

**Hybrid contribution without decomposition or explicit framing.** The paper makes two co-equal claims without satisfying the full validation requirements of either. *Corrective action:* Identify the primary contribution, reduce the secondary contribution to a supporting role, and add a paragraph in the introduction that explicitly scopes what is and is not being claimed for each.

**Type-venue mismatch.** A mature empirical study is submitted to a venue that primarily accepts system or theory papers; or a vision paper is submitted to a venue that requires rigorous empirical validation. *Corrective action:* Study accepted paper profiles, not just scope statements, for your target venue. Many venues nominally accept multiple paper types but have de facto acceptance cultures that favor one or two types.

**SLR submitted as survey.** A protocol-driven systematic review is submitted under the "survey" label and evaluated against coverage and classification criteria rather than protocol rigor and evidence synthesis criteria. *Corrective action:* Explicitly identify the paper as a systematic literature review in the title or abstract, cite the protocol (including exclusion criteria), and report inter-rater reliability for the classification step (Kitchenham et al., 2009).

**Replication without replication type declaration.** A replication study does not state whether it is an exact or conceptual replication, leading to reviewer confusion about whether operational differences are bugs or features. *Corrective action:* Adopt Carver et al.'s (2014) terminology explicitly: state the replication type, list the operational differences from the original, and justify each difference as intentional or unavoidable.

---

## 9. Worked Examples

The following examples apply the full decision protocol to representative research scenarios. They are illustrative, not exhaustive.

---

**Example A: A New Scheduling Algorithm for Real-Time Systems**

*Contribution:* A new algorithm that provably meets hard deadlines under a broader class of task sets than existing schedulers, implemented and benchmarked on embedded hardware.

*Novelty analysis:* Conceptual novelty (new scheduling criterion) — incremental. Technical novelty (new algorithm with formal correctness proof) — incremental. Empirical novelty (evaluation on embedded platform) — application. Application novelty — moderate.

*Paper type:* Full research paper.

*Model type:* Formal model (algorithm specification and correctness proof) + system model (implementation) + experimental model (hardware benchmark with comparison to prior schedulers). The formal proof addresses correctness; the benchmark addresses practical utility.

*Validation requirement:* The proof must be complete; the benchmark must compare against the closest prior schedulers on the same hardware; the experimental section must characterize edge cases where the new scheduler underperforms.

*Venue:* Real-time systems conferences (RTSS, RTAS) or journals (Real-Time Systems).

---

**Example B: A Mixed-Method Study of Code Review Practices with a Derived Taxonomy**

*Contribution:* A large-scale mixed-method study combining repository mining with developer interviews, producing statistical findings on review latency and a grounded taxonomy of review decision factors.

*Novelty analysis:* Empirical novelty (large-scale mixed-method design combining mining and interviews) — incremental to moderate. Conceptual novelty (derived taxonomy) — application/reconceptualizing.

*Hybrid assessment:* This is a Configuration 2 hybrid (Empirical Study + Conceptual Framework). The taxonomy is a derived artifact of the study, not an independent contribution of equal weight.

*Recommendation:* Submit as a full research paper with the empirical study as the primary contribution. Frame the taxonomy as a "theoretical contribution grounded in empirical evidence" rather than a co-equal contribution. If the taxonomy is subsequently applied and validated independently, a conceptual paper can be written citing this paper as empirical grounding.

*Model type:* Statistical model (mixed-method design, grounded theory coding for interviews, quantitative analysis for mining) + conceptual framework (taxonomy with discriminative definitions).

*Venue:* ICSE, FSE, MSR, or TSE/EMSE.

---

**Example C: A New Domain-Specific Language for Specifying Security Policies**

*Contribution:* A new DSL with a formal semantics, a compiler, and a case study demonstrating its application to three real-world access control systems.

*Novelty analysis:* Conceptual novelty (language design and formal semantics) — incremental. Technical novelty (compiler) — incremental. Application novelty (security policy domain) — moderate.

*Hybrid assessment:* This is a Configuration 1 hybrid (System + Methodology), where the DSL constitutes both the system artifact and the methodological contribution. Unification is appropriate here because the DSL's validation is inseparable from its application — a language without demonstrated use cases is not evaluable.

*Model type:* Formal model (operational semantics) + system model (compiler architecture) + experimental model (case study with comparative analysis against policy specification in a prior language).

*Framing recommendation:* The paper should be structured as a programming languages or security paper depending on the primary audience. If submitted to a PL venue, foreground the formal semantics and expressiveness results; if submitted to a security venue, foreground the policy expressibility and security guarantees.

*Venue:* PLDI, POPL (if formal results are strong), IEEE S&P, CCS, or USENIX Security (if security application is primary).

---

## 10. Conclusions

The original taxonomy provided a well-structured and largely accurate pedagogical framework for understanding paper types in computer science. The extensions developed in this report materially deepen that framework along two dimensions.

The contribution novelty gradient analysis demonstrates that novelty is a multidimensional construct and that the relationship between novelty claims and validation obligations is proportional and non-negotiable. A paper cannot claim disruptive novelty and provide idea-paper-level evidence; the mismatch will be detected by any competent reviewer. Equally, a paper that modestly claims incremental novelty while providing disruptive-novelty-level evidence has underframed its contribution and diminished its impact.

The hybrid contribution taxonomy identifies the five most common hybrid configurations in computing research, explains why each fails under standard single-type review, and provides resolution strategies grounded in the decomposition principles of independence, non-redundancy, sequencing, and disclosure. The decision protocol synthesizes these elements into a six-step procedure that researchers can apply before the writing process begins — the point at which framing decisions are most consequential.

Together, these extensions constitute a methodological reference suitable for use in doctoral training programs, research methodology seminars, and self-directed use by researchers at any career stage who are developing their paper framing judgment.

---

## 11. References

ACM Artifact Review and Badging. (2020). *Artifact review and badging policy (Version 1.1)*. Association for Computing Machinery. https://www.acm.org/publications/policies/artifact-review-and-badging-current

Carver, J. C., Juristo, N., Baldassarre, M. T., & Vegas, S. (2014). Replications of software engineering experiments. *Empirical Software Engineering, 19*(2), 267–276. https://doi.org/10.1007/s10664-013-9290-8

Dijkstra, E. W. (1968). Go to statement considered harmful. *Communications of the ACM, 11*(3), 147–148. https://doi.org/10.1145/362929.362947

Fanelli, D. (2010). "Positive" results increase down the hierarchy of the sciences. *PLOS ONE, 5*(4), e10068. https://doi.org/10.1371/journal.pone.0010068

Gebru, T., Morgenstern, J., Vecchione, B., Vaughan, J. W., Wallach, H., Daumé, H., III, & Crawford, K. (2021). Datasheets for datasets. *Communications of the ACM, 64*(12), 86–92. https://doi.org/10.1145/3458723

Gregor, S., & Hevner, A. R. (2013). Positioning and presenting design science research for maximum impact. *MIS Quarterly, 37*(2), 337–355. https://doi.org/10.25300/MISQ/2013/37.2.01

Jedlitschka, A., Ciolkowski, M., & Pfahl, D. (2008). Reporting experiments in software engineering. In F. Shull, J. Singer, & D. I. K. Sjøberg (Eds.), *Guide to advanced empirical software engineering* (pp. 201–228). Springer. https://doi.org/10.1007/978-1-84800-044-5_8

Kitchenham, B., Brereton, O. P., Budgen, D., Turner, M., Bailey, J., & Linkman, S. (2009). Systematic literature reviews in software engineering — A systematic literature review. *Information and Software Technology, 51*(1), 7–15. https://doi.org/10.1016/j.infsof.2008.09.009

Parnas, D. L. (1972). On the criteria to be used in decomposing systems into modules. *Communications of the ACM, 15*(12), 1053–1058. https://doi.org/10.1145/361598.361623

Paullada, A., Raji, I. D., Bender, E. M., Denton, E., & Hanna, A. (2021). Data and its (dis)contents: A survey of dataset development and use in machine learning research. *Patterns, 2*(11), 100336. https://doi.org/10.1016/j.patter.2021.100336

Shull, F., Singer, J., & Sjøberg, D. I. K. (Eds.). (2008). *Guide to advanced empirical software engineering*. Springer. https://doi.org/10.1007/978-1-84800-044-5

Wieringa, R. J. (2014). *Design science methodology for information systems and software engineering*. Springer. https://doi.org/10.1007/978-3-662-43839-8

---

*This document is intended as a living reference. Researchers are encouraged to annotate it with venue-specific observations and contribute additional hybrid configurations as they are encountered in practice.*
