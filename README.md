# FERN
## Free-Energy Register Navigation
### Collective Model Expansion Under Active Inference: A Framework for Collective Sense-Making in Complex Problem Environments

---

> *"The internal states of a particular system move in a space of beliefs — that is, on a statistical manifold."*
> — Ramstead et al., Bayesian Mechanics, Interface Focus 2023

> *"We chart a path to a generalization covering systems that exist far from equilibrium and elude steady-state densities — an area of study we designate as G-theory."*
> — Ramstead et al., 2023

> *"The solution cannot be known before the work begins, because the work is what makes the solution possible."*

---

## What This Is

FERN is a formal framework for collective sense-making in complex problem environments, derived from the mathematics of active inference and Bayesian mechanics. It occupies a specific, identified gap in the existing literature: the far-from-equilibrium collective inference regime that Ramstead et al. (2023) designate as G-theory and leave as future work.

Where prior active inference models characterize how collectives converge — how agents align posteriors, form epistemic communities, and consolidate shared beliefs — FERN characterizes the complementary regime: the conditions under which a collective must not converge but structurally expand its generative model. Not update parameters within an existing structure. Change the structure itself.

FERN derives two core formal results in this regime and maps them onto the practice of collective sense-making with explicit consequences for how collectives should be designed and facilitated:

**FERN-T1** *(Complexity Criterion)* — a formal threshold condition distinguishing when parameter updating within an existing model is adequate from when model depth expansion is the required inference strategy.

**FERN-T2** *(Democratic Weighting as Marginal Model Evidence)* — a proof that the epistemically optimal weight for any contribution to a collective learning process is its marginal increase in collective Bayesian model evidence, a quantity independent of the contributor's institutional credentials.

Both theorems are conditional on FERN-C1, the load-bearing conjecture that the space of epistemic contributions in collective learning constitutes a statistical manifold under the Fisher-Rao metric. The proof strategy for FERN-C1 is stated. The theorems stand as formally derived results under that conjecture.

FERN is a companion framework to FELD (*Field-Emergent Learning Dynamics*) and ODES (*Ordered Divergence in Expressive Space*). Where FELD derives the structural requirements of collective sense-making from non-equilibrium thermodynamics, FERN grounds the same requirements in the mathematics of active inference and information geometry, producing formally distinct but structurally convergent results.

---

## Contents

- [Provenance](#provenance)
- [Part I — The Problem Space](#part-i--the-problem-space)
- [Part II — The Statistical Manifold of Collective Generative Models](#part-ii--the-statistical-manifold-of-collective-generative-models)
- [Part III — The Complexity Criterion](#part-iii--the-complexity-criterion)
- [Part IV — Free Energy Barriers as Assumption Ridges](#part-iv--free-energy-barriers-as-assumption-ridges)
- [Part V — Diversity as Mean Pairwise KL Divergence](#part-v--diversity-as-mean-pairwise-kl-divergence)
- [Part VI — Democratic Weighting as Model Evidence](#part-vi--democratic-weighting-as-model-evidence)
- [Part VII — Shared Observability as the Collective Markov Blanket Condition](#part-vii--shared-observability-as-the-collective-markov-blanket-condition)
- [Part VIII — The Iterative Probe-Commit Cycle](#part-viii--the-iterative-probe-commit-cycle)
- [Part IX — Positioning in the Literature](#part-ix--positioning-in-the-literature)
- [Part X — Theorems, Conjectures, and Working Hypotheses](#part-x--theorems-conjectures-and-working-hypotheses)
- [Part XI — Summary of Claims](#part-xi--summary-of-claims)
- [Citations](#citations)

---

## Provenance

The Bayesian mechanics research program has built a rigorous foundation for understanding systems that behave as if they are performing Bayesian inference. Bayesian mechanics is a probabilistic mechanics comprising tools that enable modeling of systems where internal states encode the parameters of beliefs — providing a formal language for modeling the constraints, forces, fields, and potentials that determine how the internal states of such systems move in a space of beliefs, on a statistical manifold.

The literature contains three main applications of Bayesian mechanics: path-tracking dynamics, mode-tracking, and mode-matching. All three describe systems at or near non-equilibrium steady state — systems whose belief dynamics converge, track, or match some stable attractor in the statistical manifold. Ramstead et al. (2023) explicitly identify the next open domain: systems that exist far from equilibrium and elude steady-state densities, which they designate G-theory, covering the duality of Bayesian mechanics of paths and entropy on paths.

The active inference literature has also studied collective dynamics. Albarracin et al. (2022) build a multi-agent active inference model of epistemic community formation, showing that once agents have reached a certain level of certainty about their beliefs, it becomes very difficult to get them to change their views — a system of self-confirming beliefs upheld by the evolving relationship between an agent's beliefs and observations. This work models the convergence regime: the conditions under which collective belief systems consolidate, polarize, and form echo chambers.

**FERN occupies the complementary territory.** Where Albarracin et al. model what happens when a collective's generative model becomes too certain and fails to update, FERN models the conditions under which a collective must structurally expand its generative model — not update parameters within an existing structure, but change the structure itself. This is the regime that Ramstead et al. flag as G-theory and leave open: far-from-equilibrium collective inference in complex problem environments, where no steady-state solution is adequate and model depth expansion is the required dynamics.

---

## Part I — The Problem Space

### 1.1 Two Regimes of Collective Inference

Active inference agents minimize variational free energy F through two channels: **perception** (updating beliefs to better fit observations) and **action** (changing observations to fit beliefs). In a collective of agents sharing a generative model, this produces coherent joint inference — agents align their posteriors, share sufficient statistics, and reduce collective surprise.

This is the correct dynamics for problems where an adequate generative model exists at the current model depth and the task is to update its parameters. The collective converges on the best available representation of the world within its current model structure.

The dynamics breaks down for a well-defined class of problems — those in which no model at the current depth is adequate:

- Observations cannot be explained by any parameterization of the current model structure
- Parameter updating within the existing model reduces F locally but leaves irreducible residual free energy F* that cannot be eliminated without changing the model structure
- The problem itself changes in response to each intervention, so no fixed model converges

These are **complex problems** in the technical sense. Not merely large or difficult problems with known solution structures. Problems where the model structure itself is the constraint.

For these problems, collective inference requires **model depth expansion** — moving from a generative model of depth h to a generative model of depth h+1, capable of representing a new level of causal abstraction. This is not a parameter update. It is a structural change. And its dynamics are governed by a different regime of active inference than the convergence dynamics that the existing literature primarily studies.

### 1.2 Why This Matters for Practice

The difference between parameter updating and model expansion is not academic. In organizational settings:

**Parameter updating** looks like: refining understanding, gathering more evidence, improving analysis, reaching a better-informed version of the prior conclusion. The structure of the question does not change; the answer gets more precise.

**Model expansion** looks like: the question turns out to be wrong. The frame through which the problem was understood turns out to be the obstacle. A contribution from outside the existing framework reveals that the problem has a structure the prior model could not represent. The structure of the question changes.

The practical failure mode is treating a problem that requires model expansion as a problem that requires parameter updating: gathering more evidence, doing more analysis, consulting more experts within the existing framework — all of which reduces F within the current model depth while leaving irreducible residual free energy that the model cannot eliminate.

FERN provides a formal criterion for identifying which regime a problem is in, and derives the structural requirements — diversity, democratic weighting, shared observability, and iterative probing — as consequences of the mathematics rather than as design preferences.

---

## Part II — The Statistical Manifold of Collective Generative Models

### 2.1 The Collective Generative Model

A collective of N agents, each with their own Markov blanket and generative model, can be treated as a composite system with a collective Markov blanket when the agents share sufficient statistics about their beliefs. As Friston et al. (2024) show, communicating agents that share belief statistics achieve lower collective free energy than isolated agents, with the alignment between agents' free energy minima emerging endogenously from the dynamics of interacting active inference agents.

The collective's shared generative model **M_col** is the emergent statistical structure characterizing how the collective as a whole relates to the problem environment. M_col has a hierarchical **depth h**: it can represent causal structure at h levels of abstraction. This depth is the key parameter that distinguishes collective model expansion from parameter updating.

### 2.2 The Fisher-Rao Metric and Epistemic Distance

The internal states of belief-endowed systems move on a **statistical manifold** — the space of all possible generative models equipped with an appropriate metric. The natural metric on this space is the Fisher-Rao metric:

```
G_F(θ)ᵢⱼ = E_{p(o|θ)}[∂ᵢ log p(o|θ) · ∂ⱼ log p(o|θ)]
```

By Chentsov's theorem (1982), G_F is the unique Riemannian metric on the space of probability distributions that is invariant under sufficient statistics — the only metric that measures pure informational distinguishability between models, regardless of parameterization.

The Fisher-Rao distance between two generative models measures exactly how much new information one model contains about the world that the other does not. This is the correct measure of the informational distance between contributions in a collective learning process: **a contribution's epistemic value is its Fisher-Rao distance from the current collective model state.**

This identification — epistemic distance = Fisher-Rao distance — is the load-bearing claim on which FERN's formal results depend.

**Conjecture [FERN-C1]** *(Epistemic Distance Identification)*. The epistemic distance `D_g(q, S_t)` between a contribution `q` and the accumulated collective knowledge state `S_t` is proportional to the Fisher-Rao distance `D_F(θ_t, θ_t + δθ_q)` between the current collective generative model and the model updated by incorporating contribution `q`:

```
D_g(q, S_t)  ∝  D_F(θ_t, θ_t + δθ_q)  =  Δ log p(o | θ)  +  O(δθ²)
```

where the second equality holds to second order in the Fisher information expansion.

This is stated as a framework conjecture rather than a theorem because proving it requires showing that the space of epistemic contributions in a human collective learning process constitutes a statistical manifold in the measure-theoretic sense. This is identified as the primary open formal problem.

### 2.3 Epistemic Register as Hierarchical Model Depth

The epistemic registers of collective sense-making correspond to hierarchical depths of the collective generative model. A hierarchical active inference model at depth h represents causes at h levels of abstraction; contributions that require representing causes at depth h+1 cannot be accommodated by the existing model structure and require expansion.

| Register | Mode of Knowing | Generative Model Depth |
|---|---|---|
| ρ₀: Tacit | Embodied, pre-reflective | h₀: sensory prediction |
| ρ₁: Experiential | Direct encounter with the problem | h₁: first-level hidden states |
| ρ₂: Conceptual | Named frameworks and analysis | h₂: second-level (causes of observations) |
| ρ₃: Systemic | Feedback patterns across cases | h₃: third-level (causes of causes) |
| ρ₄: Propositional | Formal testable hypotheses | h₄: parametric causal structure |
| ρ₅: Metamodeling | Claims about limits of prior models | h₅: meta-level (model of the model) |

A transition from ρ_n to ρ_{n+1} in collective sense-making corresponds to an expansion of M_col from depth h_n to h_{n+1}. This is not a parameter update within the existing model. It requires a structural change to M_col that introduces a new level of causal representation.

---

## Part III — The Complexity Criterion

### 3.1 When Model Expansion Is Required

Let `F*_col(h)` denote the minimum achievable collective variational free energy at model depth h — the residual free energy that cannot be eliminated by any parameter updating within the current model structure. Let `C_expand(h → h+1)` denote the cost of expanding M_col from depth h to depth h+1: the energetic cost of restructuring the collective's shared generative model, including the temporary elevation of collective F during the transition.

**Theorem [FERN-T1]** *(Complexity Criterion)*. Model expansion from depth h to depth h+1 is required — and parameter updating within depth h is insufficient — if and only if:

```
F*_col(h)  >  C_expand(h → h+1)
```

When residual free energy at the current model depth exceeds the cost of model expansion, the optimal collective inference strategy is expansion rather than further parameter updating within the existing model structure.

**Proof sketch.** Under the FEP, the optimal collective inference minimizes expected free energy. The total expected free energy over the inference horizon is:

```
∫ F_col dt  =  ∫ F*_col(h) dt  +  C_expand     [if expansion occurs]
∫ F_col dt  =  ∫ F*_col(h) dt                   [if expansion does not occur]
```

The expansion path has lower total expected free energy if and only if the reduction in `F*_col` achieved by expanding — from `F*_col(h)` to `F*_col(h+1) < F*_col(h)` — integrated over the remaining inference horizon exceeds `C_expand`. In the limit where `F*_col(h+1) ≈ 0` and the inference horizon is sufficiently long, this reduces to `F*_col(h) > C_expand(h → h+1)`. ∎

*Note: A complete proof requires specifying the path integral formulation of collective free energy across the model expansion, which depends on the topology of the statistical manifold M_G in the neighborhood of the expansion barrier. This is identified as a primary target for formal development.*

### 3.2 The Two Failure Modes

The Complexity Criterion is an operational decision rule. It identifies when to stop optimizing within the current framing and when to pursue structural change to the framing itself. It has two failure modes in practice:

**Underexpansion:** `F*_col(h) > C_expand` but the collective continues parameter updating, treating the residual free energy as a data-gathering problem. This produces the accumulation of evidence that does not change the conclusion, the analysis that keeps generating the same recommendations, the expert consultation that produces agreement within a framework that is itself the problem.

**Premature expansion:** `C_expand > F*_col(h)` but the collective pursues model restructuring, abandoning a framework that was still adequate. This produces instability, loss of accumulated understanding, and the permanent occupation of the transition cost without the benefit of an improved model.

The Complexity Criterion provides the formal distinction between these two errors.

---

## Part IV — Free Energy Barriers as Assumption Ridges

### 4.1 The Barrier Structure of the Statistical Manifold

Between the attractor basin of a depth-h model and the attractor basin of a depth-(h+1) model in the statistical manifold M_G lies a region of elevated collective free energy: the **expansion barrier**. Moving from depth h to depth h+1 requires the collective to temporarily occupy this high-F region — a state of productive uncertainty in which the prior model structure is no longer organizing collective inference and the new structure has not yet been adopted.

**Conjecture [FERN-C2]** *(Barrier Height)*. The expansion barrier height between model depths h and h+1 is:

```
C_expand(h → h+1)  =  max_{γ: h → h+1} F_col(γ(t))  −  F*_col(h)
```

where the maximum is taken over all paths γ in M_G connecting the depth-h attractor to the depth-(h+1) attractor. The minimum-cost path — the geodesic through the barrier — is the saddle point of F_col between the two attractor basins.

The assumption ridge identified in collective sense-making practice is the free energy barrier between model depth h and model depth h+1. Crossing it requires the collective to sustain elevated uncertainty — elevated F_col — without prematurely resolving it through convergence to the prior model.

**This makes the facilitator's role precise:** maintain shared observability of the high-F transition state long enough for the expansion to complete. Facilitation that reduces uncertainty prematurely — that moves toward consensus before the barrier has been crossed — pushes the collective back into the depth-h basin, restoring the prior model at the cost of the expansion.

### 4.2 Why High-Precision Priors Block Expansion

Albarracin et al. show that once agents have a high level of certainty about their beliefs, it becomes very difficult for them to change their views — a system of self-confirming beliefs upheld by the evolving relationship between agents' beliefs and observations. In FERN terms, high-precision priors at depth h reduce the agent's sensitivity to the evidence that `F*_col(h) > 0` — the evidence that the current model is inadequate. The agent's high-precision model interprets observations that should register as residual free energy as noise, absorbs them as minor parameter adjustments, and remains in the depth-h basin.

**The precision of priors is therefore the primary determinant of `C_expand` from the agents' side:** high-precision institutional priors, professional consensus, and prior successful solutions all elevate the effective expansion cost by reducing agents' sensitivity to the evidence that expansion is required.

Contributions from agents with low-precision, high-proximity models of the problem — agents whose generative models have been calibrated directly against the problem rather than through institutional frameworks — have lower effective prior precision. They are more sensitive to the evidence of model inadequacy. They register `F*_col(h)` more accurately. This is the mechanism by which direct experience contributes to assumption rupture that expert analysis cannot produce: not because the experiential model is more accurate, but because its priors are less certain, making it more sensitive to the evidence that the existing framing is failing.

---

## Part V — Diversity as Mean Pairwise KL Divergence

### 5.1 Formal Definition

**Conjecture [FERN-C3]** *(Diversity and Entropy Production Rate)*. Let `A = {a₁, ..., a_N}` be a group of N agents with generative models `p(·|θᵢ)`. The epistemic diversity of the group is the **mean pairwise KL divergence** between individual generative models:

```
D_FERN(A)  =  (1/N²) Σᵢⱼ DKL[p(·|θᵢ) || p(·|θⱼ)]
```

The rate of collective epistemic entropy production is bounded below by:

```
dH_col/dt  ≥  α · D_FERN(A) · Σᵢ P(qᵢ | S_t)
```

for some `α > 0`, where `P(qᵢ|S_t)` is the epistemic pressure at each agent's current contribution position.

This lower bound is achieved when agents navigate from their current positions toward the high-pressure regions of the collective statistical manifold — when each agent's contribution moves M_col toward unexplored territory in the direction of highest model evidence gain.

### 5.2 Why This Formalizes the Diversity Claim

`DKL[pᵢ||pⱼ]` measures how much agent i's generative model would be surprised by agent j's predictions. Agents with structurally non-overlapping generative models — different hierarchical depths, different prior structures, different domains of calibration — have high mutual KL divergence. Their encounter produces high information transfer: each agent's contributions are far from the other's current model, producing large Fisher-Rao displacements of M_col.

This makes precise what "cognitive diversity" means in the context of complex collective learning: not diversity of opinion within a shared model structure, but **structural diversity of generative models** across the agents of the collective.

Two expert economists with different views have low D_FERN — their models are structurally similar, differing in parameter values rather than depth or causal structure. An economist, a community health worker, and a directly affected resident have high D_FERN — their models are calibrated at different hierarchical depths, with different prior structures, representing the problem with different causal architectures.

High D_FERN does not guarantee high entropy production — agents must also be able to contribute from their current positions and those contributions must be receivable by the collective. But the bound makes clear that `D_FERN = 0` (structurally homogeneous group) guarantees that collective entropy production is limited to what a single generative model structure can access.

---

## Part VI — Democratic Weighting as Model Evidence

### 6.1 The Core Result

**Theorem [FERN-T2]** *(Democratic Weighting as Marginal Model Evidence)*. Under FERN-C1, the epistemic value of a contribution `q` — its distance from the current collective knowledge state — is proportional to the marginal increase in collective Bayesian model evidence produced by incorporating that contribution into M_col:

```
D_g(q, S_t)  ∝  Δ log p(o | θ_t + δθ_q)  −  Δ log p(o | θ_t)
```

to second order in δθ. This quantity is independent of the institutional credentials of the contributor.

**Proof.** Under FERN-C1, `D_g(q, S_t) = D_F(θ_t, θ_t + δθ_q)`. The Fisher-Rao distance to second order in δθ is:

```
D_F(θ_t, θ_t + δθ_q)  =  √(δθ_q^T G_F(θ_t) δθ_q)  +  O(δθ³)
```

By the information geometry of exponential families, the Fisher-Rao metric G_F(θ) governs the curvature of the log-likelihood landscape. To second order:

```
Δ log p(o | θ_t + δθ_q)  ≈  ∇_θ log p(o|θ_t)^T δθ_q  +  ½ δθ_q^T ∇²_θ log p(o|θ_t) δθ_q
```

The Fisher information matrix is `F(θ) = −E[∇²_θ log p(o|θ)]`, so `G_F(θ) = F(θ)`. The marginal model evidence gain is therefore:

```
Δ log p(o | θ)  ≈  ½ δθ_q^T G_F(θ_t) δθ_q  =  ½ D_F²(θ_t, θ_t + δθ_q)
```

to second order, establishing `D_g ∝ Δ log p(o|θ)`. ∎

*Note: This proof holds under the assumptions of FERN-C1 and in the second-order approximation. Both conditions require additional justification for the general case of human collective learning processes.*

### 6.2 What This Means

Model evidence — the probability of observations under a generative model, integrated over all parameter values — is a property of the model, not the person who contributed to it. A contribution that moves M_col to a region of the statistical manifold with higher model evidence is epistemically valuable. A contribution that moves M_col to a region with lower model evidence is not. This has nothing to do with who made the contribution.

**The democratic weighting result is not an egalitarian principle. It is a measurement consequence:** in collective inference aimed at accurate understanding of a complex problem, the epistemically optimal weight to assign a contribution is its marginal model evidence gain, and this is independent of the contributor's institutional position.

In practice this means that direct-experience contributions from people calibrated against the problem environment at low hierarchical levels (ρ₀–ρ₁) provide model evidence gains in those levels that no amount of expert analysis at higher levels (ρ₂–ρ₄) can produce — because high-level conceptual models have already compressed away the variance at lower levels, and model evidence at those lower levels requires reinstating it.

---

## Part VII — Shared Observability as the Collective Markov Blanket Condition

### 7.1 The Necessity

A collective Markov blanket exists only when the internal states of the collective — the shared generative model M_col and its sufficient statistics — are jointly accessible to all agents through collective sensory states. As Friston et al. (2024) show, each agent in a communicating collective achieves lower free energy, with alignment between agents' free energy minima emerging endogenously from their interactions. This endogenous alignment requires that agents can observe each other's sufficient statistics: the shared blanket states.

**Conjecture [FERN-C4]** *(Blanket State Observability)*. The collective Markov blanket — and therefore the collective generative model M_col — exists as a coherent inferential unit if and only if all agents have access to the collective's blanket states: the sufficient statistics of the current shared model, the accumulated contributions to it, and the collective's current uncertainty about the problem.

Without this access, agents are performing individual inference on their private sensory states, not collective inference on the shared model. They navigate the pressure landscape of their own priors, not the collective statistical manifold. Individual contributions do not update M_col because M_col is not observable to the contributing agents.

**The practical implementation of this condition — shared documentation, visible synthesis, public uncertainty — is not organizational scaffolding. It is the structural requirement for the collective Markov blanket to exist at all.**

### 7.2 The Line-of-Sight Condition in Practice

Albarracin et al. show that agents are driven by the epistemic value of sampling the behaviors of other agents, and that who they attend to and what they read influences their beliefs about the world. Extending this to the model expansion regime: agents in a collective navigating a complex problem must be able to observe not just each other's conclusions but the current state of the shared model M_col — where it is adequate, where its residual free energy is concentrated, and which regions of the statistical manifold are high-pressure.

Line-of-sight is how the swarm remains a swarm rather than fragmenting into independent agents.

---

## Part VIII — The Iterative Probe-Commit Cycle

### 8.1 Epistemic Foraging in the Expansion Regime

In the model expansion regime, the collective's primary challenge is identifying which direction in the statistical manifold the expansion should take — which new model depth structure reduces `F*_col` most efficiently. This requires probing the manifold before committing to a new model structure.

Active inference distinguishes **epistemic actions** (designed to reduce uncertainty about the state of the world and the model) from **pragmatic actions** (designed to achieve preferred outcomes). In the model expansion regime, the collective primarily requires epistemic actions: exploratory contributions that map the territory of the statistical manifold without yet committing to a new model structure.

**Type I contributions** are permanent model updates: contributions that, when incorporated into M_col, produce sufficient `Δ log p(o)` to cross the threshold for lasting integration. These are model-expanding commitments.

**Type II probes** are epistemic actions: exploratory contributions that probe the local topology of M_G — what model structures are available in the neighborhood of the current position — without yet committing to them.

The just-in-time structure of emergent learning is a consequence of this cycle: the high-pressure regions of the statistical manifold — the directions where model evidence can most be increased — self-reveal through the collective's existing residual free energy, without requiring advance knowledge of which contributions will be most valuable.

---

## Part IX — Positioning in the Literature

FERN extends the Bayesian mechanics and active inference literature in one specific direction: the far-from-equilibrium collective inference regime that Ramstead et al. (2023) identify as G-theory and leave as future work.

The existing literature primarily characterizes:

- Individual FEP dynamics (parameter updating within a fixed model structure)
- Mode-matching and mode-tracking collective dynamics (convergence to shared attractors)
- Echo chamber formation under high-precision priors (Albarracin et al. 2022 — the failure mode of collective inference)

FERN characterizes the **complementary regime**: the conditions under which collective model depth expansion is optimal, the formal criterion for identifying those conditions (FERN-T1), and the structural requirements for model expansion to occur — diversity as high D_FERN, democratic weighting as marginal model evidence, and shared observability as the collective Markov blanket condition.

**The primary open formal problem** is the proof of FERN-C1: that the space of epistemic contributions in collective sense-making processes constitutes a statistical manifold in the measure-theoretic sense required to apply the Fisher-Rao metric. Without this proof, FERN-T1 and FERN-T2 rest on FERN-C1 as a conjecture. The proof strategy is to show that each contribution can be represented as a sufficient statistic update to a parametric generative model, then apply Chentsov's theorem to establish the Fisher-Rao metric as the unique invariant metric.

**The primary open empirical problem** is measurement of D_FERN in real collectives and correlation with entropy production rate. A clean experiment measuring pairwise KL divergence between team members' generative models — operationalized as divergence in causal structure maps elicited before a complex problem session — and correlating it with the rate of novel insight production during the session would be the first empirical test of the framework's central prediction.

---

## Part X — Theorems, Conjectures, and Working Hypotheses

### Formally Derived Results

| ID | Statement | Status |
|---|---|---|
| FERN-T1 | **Complexity Criterion:** model expansion required iff `F*_col(h) > C_expand(h→h+1)`; parameter updating insufficient above this threshold | [T] *(proof sketch; full proof requires path integral formulation of collective F)* |
| FERN-T2 | **Democratic Weighting:** `D_g(q,S_t) ∝ Δ log p(o|θ)` to second order under FERN-C1; epistemic value = marginal model evidence gain, independent of contributor credentials | [T] *(conditional on FERN-C1)* |

### Conjectures

| ID | Statement | Status |
|---|---|---|
| FERN-C1 | **Epistemic Distance Identification:** `D_g(q,S_t) ∝ D_F(θ_t, θ_t+δθ_q)`; the space of collective epistemic contributions constitutes a statistical manifold under the Fisher-Rao metric | [C] *(load-bearing; proof strategy: sufficient statistics + Chentsov)* |
| FERN-C2 | **Barrier Height:** expansion barrier `C_expand = max F_col` along geodesic between depth-h and depth-(h+1) attractors; the saddle point of F_col between the two basins | [C] |
| FERN-C3 | **Diversity Bound:** `dH_col/dt ≥ α · D_FERN · Σ P(qᵢ|S_t)`; mean pairwise KL divergence between generative models lower-bounds entropy production rate | [C] |
| FERN-C4 | **Blanket Observability:** collective Markov blanket exists iff all agents have access to the collective's sufficient statistics; loss of line-of-sight = fragmentation of collective inferential unit | [C] |
| FERN-C5 | **Expansion Irreversibility:** once collective model depth expands from h to h+1, return to depth h is blocked by the anti-ergodic accumulation of model evidence at h+1; the depth-h attractor is no longer accessible | [C] |

### Working Hypotheses

| ID | Statement | Status |
|---|---|---|
| FERN-H1 | High-precision institutional priors elevate effective `C_expand` by reducing agents' sensitivity to `F*_col(h) > 0`; this is the mechanism by which successful prior solutions become the primary obstacle to solving novel complex problems | [H] |
| FERN-H2 | Direct-experience contributors (ρ₀–ρ₁) have structurally lower prior precision than domain experts (ρ₂–ρ₄) because their models were calibrated against the problem directly rather than through institutional compression; this makes them more sensitive to `F*_col(h) > 0` and more likely to register the evidence that model expansion is required | [H] |
| FERN-H3 | The time to first register escape t* in a collective scales inversely with D_FERN: more structurally diverse collectives cross expansion barriers earlier, as a consequence of the higher KL divergence signals reaching agents near the barrier | [H] |
| FERN-H4 | The far-from-equilibrium regime characterized here — model depth expansion, anti-ergodic accumulation, no steady-state — is the formal instantiation of Ramstead et al.'s G-theory applied to human collective learning processes | [H] |

---

## Part XI — Summary of Claims

The framework makes three claims, ordered by their epistemic status.

**The established claim** (FERN-T2, conditional on FERN-C1): If epistemic contributions can be represented as updates to a collective generative model on a statistical manifold, then the epistemically optimal weight for any contribution is its marginal increase in collective Bayesian model evidence — a quantity that is independent of the contributor's institutional credentials and that formalizes democratic weighting as a measurement consequence rather than a value preference.

**The core formal conjecture** (FERN-T1): There exists a threshold condition separating parameter updating (the adequate regime for simple problems) from model depth expansion (the required regime for complex problems), expressible in terms of residual collective free energy and expansion barrier height. Above this threshold, further parameter updating within the existing model is the wrong inference strategy regardless of how much evidence is gathered.

**The empirical prediction**: Structural diversity between collective members — measured as mean pairwise KL divergence between individual generative models — lower-bounds the rate of genuine collective learning in complex problem environments. Collectives with `D_FERN ≈ 0` cannot exceed the learning rate of a single generative model structure. This is a falsifiable prediction about real collectives that can be tested without resolving FERN-C1.

---

## Citations

**Free Energy Principle, Active Inference, and Bayesian Mechanics**

Friston, K. (2010). The free-energy principle: a unified brain theory? *Nature Reviews Neuroscience* 11(2): 127–138.

Friston, K., Da Costa, L., Tschantz, A., et al. (2024). Designing ecosystems of intelligence from first principles. *Collective Intelligence* 3(1).

Ramstead, M.J.D., Sakthivadivel, D.A.R., Heins, C., Koudahl, M., Millidge, B., Da Costa, L., Klein, B., and Friston, K. (2023). On Bayesian mechanics: a physics of and by beliefs. *Interface Focus* 13(3): 20220029.

Da Costa, L., Friston, K., Heins, C., and Pavliotis, G.A. (2021). Bayesian mechanics for stationary processes. *Proceedings of the Royal Society A* 477: 20210518.

Kirchhoff, M., Parr, T., Palacios, E., Friston, K., and Kiverstein, J. (2018). The Markov blankets of life: autonomy, active inference and the free energy principle. *Journal of the Royal Society Interface* 15(138): 20170792.

Friston, K., Parr, T., Heins, C., et al. (2024). Federated inference and belief sharing. *Neuroscience and Biobehavioral Reviews* 156: 105500.

**Collective Dynamics under Active Inference**

Albarracin, M., Demekas, D., Ramstead, M.J.D., and Heins, C. (2022). Epistemic communities under active inference. *Entropy* 24(4): 476.

**Information Geometry**

Amari, S. (2016). *Information Geometry and Its Applications.* Springer.

Chentsov, N.N. (1982). *Statistical Decision Rules and Optimal Inference.* American Mathematical Society.

**Collective Intelligence**

Barfuss, W., Flack, J.C., Gokhale, C., et al. (2023). Collective cooperative intelligence. *Proceedings of the National Academy of Sciences* 120(8): e2209561120.

Hong, L. and Page, S.E. (2004). Groups of diverse problem solvers can outperform groups of high-ability problem solvers. *Proceedings of the National Academy of Sciences* 101(46): 16385–16389.

Page, S.E. (2007). *The Difference: How the Power of Diversity Creates Better Groups, Firms, Schools, and Societies.* Princeton University Press.

**Non-Equilibrium Dynamics**

Prigogine, I. and Nicolis, G. (1977). *Self-Organization in Non-Equilibrium Systems.* Wiley.

**Collective Learning Practice**

Snowden, D.J. and Boone, M.E. (2007). A leader's framework for decision making. *Harvard Business Review* 85(11): 68–76.

Patton, M.Q. (2011). *Developmental Evaluation: Applying Complexity Concepts to Enhance Innovation and Use.* Guilford Press.

Wenger, E. (1998). *Communities of Practice: Learning, Meaning, and Identity.* Cambridge University Press.

---

*Framework: FERN · FELD · ODES*

*Status tags: [T] = Theorem (with stated conditions and proof sketch) · [C] = Open conjecture · [H] = Working hypothesis*

*Primary open formal problem: Proof of FERN-C1 (the epistemic-distance–Fisher-Rao identification), on which FERN-T1 and FERN-T2 are conditional. Proof strategy: represent collective epistemic contributions as sufficient statistics of a parametric generative model; apply Chentsov's theorem for the uniqueness of the Fisher-Rao metric; establish the second-order model evidence expansion.*

*Primary empirical target: Measurement of D_FERN (mean pairwise KL divergence between team members' generative models) and correlation with collective entropy production rate in real complex problem-solving sessions.*
