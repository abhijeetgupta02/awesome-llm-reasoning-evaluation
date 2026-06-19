# Awesome LLM Reasoning Evaluation [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A curated list of benchmarks, frameworks, datasets, and research for evaluating
> the **reasoning ability** — and the **faithfulness** of that reasoning — in large
> language models and large reasoning models.

Most "reasoning" scores are a single number on a saturating benchmark. This list
collects the tools and ideas needed to evaluate reasoning *rigorously*: multi-step
correctness, chain-of-thought faithfulness, and failure analysis.

Maintained by [Abhijeet Gupta](https://github.com/abhijeetgupta02).
Contributions welcome — see [Contributing](#contributing).

## Contents

- [Frameworks & Harnesses](#frameworks--harnesses)
- [Reasoning Benchmarks](#reasoning-benchmarks)
  - [Math](#math)
  - [Science & Knowledge](#science--knowledge)
  - [Logic & Abstraction](#logic--abstraction)
- [Chain-of-Thought & Faithfulness](#chain-of-thought--faithfulness)
- [Failure Analysis & Interpretability](#failure-analysis--interpretability)
- [Leaderboards](#leaderboards)
- [Contributing](#contributing)
- [License](#license)

## Frameworks & Harnesses

- [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) — EleutherAI. The de-facto standard; backend of the Open LLM Leaderboard, 60+ tasks, used in hundreds of papers.
- [LightEval](https://github.com/huggingface/lighteval) — Hugging Face. Lightweight, backend-agnostic evaluation pipeline.
- [OpenCompass](https://github.com/open-compass/opencompass) — Broad evaluation platform spanning general, domain (finance/health/law), and reasoning benchmarks.
- [HELM](https://github.com/stanford-crfm/helm) — Stanford CRFM. Multi-metric evaluation (accuracy, calibration, robustness, bias, efficiency) in one run.
- [Inspect AI](https://github.com/UKGovernmentBEIS/inspect_ai) — UK AI Safety Institute. Framework with prompt/tool/agent support and a viewer; see the companion [inspect_evals](https://github.com/UKGovernmentBEIS/inspect_evals) collection.
- [OpenAI Evals](https://github.com/openai/evals) — Framework plus an open registry of benchmarks.
- [simple-evals](https://github.com/openai/simple-evals) — Minimal-dependency reference scripts for MMLU, GPQA, HumanEval, and more.
- [promptfoo](https://github.com/promptfoo/promptfoo) — Local-first prompt/LLM testing, scoring, and red-teaming with CI/CD integration.

## Reasoning Benchmarks

### Math

- [GSM8K](https://github.com/openai/grade-school-math) — 8.5K grade-school math word problems requiring 2–8 step arithmetic reasoning.
- [MATH](https://github.com/hendrycks/math) — Competition-level mathematics (AMC/AIME-style); the 500-problem **MATH-500** subset is a common reasoning probe.

### Science & Knowledge

- [GPQA](https://github.com/idavidrein/gpqa) — Graduate-level, "Google-proof" science QA; the **GPQA-Diamond** split is the hardest and most-cited.
- [MMLU](https://github.com/hendrycks/test) — 57-subject multitask knowledge benchmark; still a standard reference point despite saturation.

### Logic & Abstraction

- [BIG-Bench Hard (BBH)](https://github.com/suzgunmirac/BIG-Bench-Hard) — 23 challenging BIG-Bench tasks where chain-of-thought prompting matters most.
- [ARC-AGI](https://github.com/fchollet/ARC-AGI) — The Abstraction and Reasoning Corpus; few-shot fluid-intelligence puzzles resistant to memorization.

## Chain-of-Thought & Faithfulness

A model's written reasoning does not necessarily reflect the computation that
produced its answer. Evaluating **faithfulness** — not just final accuracy — is an
open and active area.

- Key idea: a chain-of-thought can be *plausible but unfaithful*, changing the
  answer without changing the stated reasoning (and vice versa).
- [Measuring the Faithfulness of Thinking Drafts in Large Reasoning Models](https://arxiv.org/abs/2505.13774) (2025) — recent work probing whether reasoning "drafts" causally drive answers.
- _Open call:_ PRs adding strong faithfulness/CoT-evaluation papers and tools are especially welcome.

## Failure Analysis & Interpretability

Aggregate accuracy hides *how* and *where* models break. Resources focused on
per-instance failure analysis:

- [reasoning-model-failure-analysis-companion](https://github.com/abhijeetgupta02/reasoning-model-failure-analysis-companion) — Sanitized public companion for forced-reconsideration LLM failure analysis, with synthetic goal-betrayal and partial-undo artifacts.
- _Open call:_ contribute interpretability tools and datasets aimed at diagnosing reasoning failures.

## Leaderboards

- [Open LLM Leaderboard](https://huggingface.co/open-llm-leaderboard) — Hugging Face; standardized leaderboard built on lm-evaluation-harness.

## Contributing

Contributions make this list better. Please read [CONTRIBUTING.md](CONTRIBUTING.md)
before opening a pull request. In short: one item per PR, keep entries factual and
non-promotional, and add a one-line description of *why* the resource matters.

## License

[![CC0](https://licensebuttons.net/p/zero/1.0/88x31.png)](LICENSE)

To the extent possible under law, the maintainers have waived all copyright and
related or neighboring rights to this work. See [LICENSE](LICENSE) (CC0 1.0).
