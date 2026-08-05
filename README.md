# PhysioFlow — Software Impacts manuscript

Source of the Original Software Publication (OSP) submitted to
[*Software Impacts*](https://www.sciencedirect.com/journal/software-impacts):

> **PhysioFlow: an open-source interactive platform for crop ecophysiology and
> agronomic data analysis with statistical and experimental-design guard-rails**

The software this manuscript describes lives in a separate repository:
**https://github.com/ML-Carbon-Project/physioFlow** — that is the repository
cited in the article's code-metadata table (C2, C8).

## Contents

| File | |
|---|---|
| `physioflow-softwareimpacts.tex` | manuscript source |
| `refs.bib` | bibliography |
| `physioflow_SoftwareImpacts_v1.pdf` | compiled manuscript |
| `figs/` | the five figures used in the manuscript |
| `Highlights.docx` | highlights (5 bullets, ≤85 characters each) |
| `cover_letter_software_impacts.docx` | cover letter |
| `declarationStatement.docx` | declaration of interests |

Build with a standard LaTeX installation (`article` class, no special class file):

```bash
pdflatex physioflow-softwareimpacts.tex
bibtex   physioflow-softwareimpacts
pdflatex physioflow-softwareimpacts.tex
pdflatex physioflow-softwareimpacts.tex
```

## How the figures were produced

The figures are screen captures of the application in use, taken by
`scripts/capture_figures.py` in the software repository, which drives the
interface with Playwright and records the resulting screens at three times the
device scale (3600 px wide, above the 2244 px Elsevier asks for at full page
width).

The field campaign of Section 3.1 belongs to an ongoing research project and
cannot be released. The figures derive from a de-identified copy of it, produced
by `scripts/deidentify_field_dataset.py` in the software repository: farm names
become `Farm A`/`Farm B`, and coordinates are relocated while the within-point
GPS jitter is preserved. **No measured value is altered**, which is why every
number in the manuscript still holds. The synthetic dataset distributed with the
software reproduces the reference *schema*, not these results, and is not the
source of any figure.

## Licence

The software is released under GPL-2.0-or-later; that licence covers the
**software repository**, not this manuscript. The text and figures here are the
work of the authors and, upon publication, are subject to the terms of the
publisher.
