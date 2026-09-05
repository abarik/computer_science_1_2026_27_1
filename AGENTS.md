# Repository Guidelines

## Project Structure & Module Organization

This repository contains the **Computer Science 1** course book for semester 2026/27/1. Root-level `.qmd` files hold course chapters; `_quarto.yml` defines chapter order, metadata, bibliography, and HTML/PDF formats. Only chapters enabled in that configuration enter the book.

- `docs/`: rendered book output; edit the corresponding sources before regenerating it.
- `labs/`: standalone HTML lab materials, named `CS_1_lab_01_files.html` through numbered sessions.
- `homework/`: assignment pages and example HTML, Word, and PowerPoint files.
- `files/`: downloadable datasets, spreadsheets, PDFs, and archives.
- `image/` and `cover.jpg`: illustrations and book cover.
- `references.bib` and `apa.csl`: bibliography and citation style.

## Build, Test, and Development Commands

Run commands from the repository root with Quarto installed:

- `quarto preview`: render and serve the book locally while editing.
- `quarto render --to html`: regenerate the HTML book in `docs/`.
- `quarto render --to pdf`: build the PDF edition; requires a working LaTeX installation.
- `quarto check`: inspect the local Quarto installation and dependencies.

Open `computer_science_1_2026_27_1.Rproj` for editing in RStudio. Standalone lab and homework HTML files also need direct browser inspection.

## Coding Style & Naming Conventions

Use UTF-8 encoding and two spaces for indentation, matching the RStudio project settings. Keep YAML indentation consistent and use descriptive Markdown headings. Follow existing lowercase, underscore-separated chapter names such as `academic_calendar.qmd`; preserve numbered lab filenames and existing download paths. Use relative links for repository assets and retain citation keys when updating bibliography entries. No formatter or linter is configured.

## Testing Guidelines

There is no automated test suite or coverage requirement. Validate changes by rendering HTML and inspecting affected pages in a browser. Check navigation, images, citations, tables, and download links. Check PDF output when changing shared layout or PDF-specific content. Review `git diff --check` and the generated diff before committing; avoid unrelated output churn.

## Commit & Pull Request Guidelines

Recent commits use short, descriptive subjects, usually beginning with verbs such as `Update`, `Fix`, or `Remove`. Keep commits focused on one course-content or presentation change. Pull requests should describe the affected pages, explain the change, and state validation performed. Link relevant issues and include screenshots for visible layout changes.
