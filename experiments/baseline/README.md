# Mozhi — Initial Tanglish Generation Baseline

## Purpose

Record the first generation experiment for Mozhi and establish a
fixed set of prompts for future model comparisons.

## Model

- Model ID: `Qwen/Qwen3-0.6B`
- Runtime: Google Colab
- GPU: NVIDIA Tesla T4
- Generation: sampling enabled, temperature 0.7, top-p 0.9
- Maximum new tokens: 120
- Test prompts: 8

## Results

See `baseline_responses.csv` for the prompts and generated responses.

The initial outputs show that the model can answer some English-heavy
technical questions, but performs poorly on natural Tanglish conversation.
Several outputs contain malformed or irrelevant romanized Tamil, and
multi-turn conversational capability has not yet been established.

## Limitations

- This is a baseline experiment, not a Tanglish fine-tuned model.
- Eight prompts are a small qualitative sample, not a comprehensive benchmark.
- No formal human evaluation or statistical quality score has been completed.
- The recovered Mozhi sentiment classifier is a separate model and was
  not modified by this experiment.
- The inference code was executed in Colab; this directory records the
  initial outputs and experiment notes.

## Next steps

1. Audit suitable Tanglish conversational training data and its license.
2. Expand the evaluation set and define consistent quality criteria.
3. Compare a specialized Tanglish model against this baseline.
4. Begin training Mozhi's small causal Transformer separately.
