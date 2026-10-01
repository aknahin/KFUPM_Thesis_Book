# KFUPM Thesis Book — LaTeX Template

A generic LaTeX template for writing an MS or PhD thesis/dissertation at King
Fahd University of Petroleum and Minerals (KFUPM), built on the official
`kfupm_thesis` class. All personal and research content has been stripped out
and replaced with placeholders, so you can clone this and start writing your
own thesis right away.

## Requirements

- A TeX distribution with `xelatex` and `latexmk` (e.g. [MacTeX](https://www.tug.org/mactex/), [TeX Live](https://www.tug.org/texlive/), or [MiKTeX](https://miktex.org/))
- An Arabic font such as **Scheherazade New** installed (used for the Arabic title/abstract pages)

## Building

```bash
latexmk -xelatex full.tex
```

This produces `full.pdf`. To clean up all generated build files:

```bash
latexmk -c
```

## Structure

| File / Folder              | Purpose                                                         |
|-----------------------------|------------------------------------------------------------------|
| `full.tex`                  | Main document — assembles the whole thesis                      |
| `title.tex`                 | Title page: thesis title, author, advisor, committee, dates     |
| `copyright.tex`             | Copyright page                                                  |
| `dedication.tex`            | Dedication page (optional, commented out by default)            |
| `ack.tex`                   | Acknowledgements                                                 |
| `abstract.tex`               | English and Arabic abstracts                                     |
| `cv.tex`                    | Vitae (author bio, education, skills, achievements)              |
| `def.tex`, `setting.tex`    | Margins, packages, and other document-wide settings — avoid editing unless you know what you're doing |
| `set_loa.tex`, `loa.tex`    | List of Abbreviations / symbols setup                            |
| `Chapters/`                 | Thesis chapters: `introduction.tex`, `literature.tex`, `methodology.tex`, `results.tex`, `conclusion.tex`, plus `references.bib` |
| `kfupm_thesis.cls`, `kfupm_thesis_ratulvai.cls` | KFUPM thesis class files — **do not modify** |
| `IEEEtran.bst`               | IEEE bibliography style used by `\bibliographystyle{IEEEtran}`  |
| `library.bib`, `library_fixed.bib` | Example/starter bibliography databases                    |

## Getting started

1. Clone this repo and rename it to your own project.
2. Edit `title.tex` — set your thesis title, name, department, advisor, and committee members.
3. Pick MS or PhD, and single- or double-sided printing, by enabling the right `\documentclass[...]` line near the top of `full.tex`.
4. Fill in `abstract.tex`, `ack.tex`, `dedication.tex` (optional), and `cv.tex` with your own content.
5. Write your chapters under `Chapters/`, and add your own figures and bibliography entries.
6. Build with `latexmk -xelatex full.tex` and iterate.

## Notes

- Enable/disable optional lines by adding or removing the leading `%` comment marker, as noted throughout the `.tex` files.
- The Arabic title/name/department/date commands (`\artitle`, `\arname`, `\ardept`, `\ardate`) are optional — comment them out if you don't need an Arabic title page.
- Refer to your department's Deanship of Graduate Studies (DGS) thesis-writing manual and LaTeX guidelines for formatting requirements specific to your program.
