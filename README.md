# Mental Health Stigma Evaluation Benchmark

A theory-grounded benchmark for the automatic evaluation of mental health stigma in online communication. It combines news and social media text with a fine-grained stigma taxonomy that includes a binary stigma-detection task and 28 categories covering the mode of stigma, its domain, and the components of particular forms of stigma. The 470 annotated excerpts mention six mental health conditions.

Paper: Automatic Evaluation of Mental Health Stigma in Online Communication, Baes et al. (2026). 

Dataset on Hugging Face: [jemimakang/mh_stigma](https://huggingface.co/datasets/jemimakang/mh_stigma)

## What is included

| File | Rows | Contents |
|---|---|---|
| `data/labels_gold.csv` | 470 | Adjudicated labels and metadata, one row per excerpt. News excerpt text is included; Reddit text is not. |
| `data/labels_annotators.csv` | 1,201 | Individual annotator labels before adjudication, one row per annotation. |
| `annotation/annotation_instructions.pdf` | — | Annotation guidelines. |
| `scripts/prototype_usages_stigma_types.csv` | — | Prototypical exemplars of stigma. |

Items are identified by `item_id` (`stig_0001`–`stig_0470`), which is consistent across all files. 

## Data sources

Excerpts come from two sources, given in the `source` column:

- `now` — excerpts from news articles in the News on the Web (NOW) corpus. Text is included in `labels_gold.csv`.
- `reddit` — excerpts from Reddit posts. Text is available on application (see below).

## Requesting the Reddit text

Reddit excerpts are released to approved researchers only, to protect against misuse and to respect platform terms. To apply, complete: https://forms.cloud.microsoft/r/KJbaMPAW03. The dataset authors review each application, usually within five working days.

Approved applicants receive `text_gated.csv`, which contains `item_id`, `text` and `stigma_span`. Join it to the label files on `item_id`.

## Annotation categories

Full definitions are documented in `annotation/annotation_instructions.pdf`.

**Stigma present**

* Yes
* No

The categories below are annotated only where stigma is present.

**Mode** 

* Expressed/enacted
* Perceived/experienced

**Domain**

* Public
* Structural
* Associative
* Self

**Public stigma type** 

* Cognitive
* Affective
* Behavioural

**Cognitive components** 

* Dangerousness
* Controllable
* Uncontrollable
* Personal responsibility and blame
* Moral or character flaw
* Pity/condescension
* Trivialisation or minimisation
* Immutability
* Segregation endorsement
* Coercion
* Contamination
* Incompetence

**Affective components** 

* Fear
* Anger, irritability or frustration
* Disgust
* Pity
* Ambivalence

**Behavioural components** 

* Social distancing

Language features were collected in the earlier rounds only. "Other" responses appear in the per-annotator file with a free-text description that is not released; during adjudication these were either recoded into a named category or left out, so the gold labels contain no "other" values.


## Citation

```bibtex
[BIBTEX ENTRY]
```


## Contact

Jemima Kang, jemimak@student.unimelb.edu.au
