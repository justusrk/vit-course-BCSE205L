# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains **Quarto RevealJS slides** for teaching **BCSE205L — Computer Architecture and Organization** at VIT. The syllabus PDF is the source of truth for all course content.

## Quarto Commands

Quarto 1.8+ is installed. Key commands:

- **Preview slides with live reload:** `quarto preview <file>.qmd`
- **Render a single file:** `quarto render <file>.qmd`
- **Render all slides:** `quarto render`

## Course Structure (from Syllabus)

Slides should follow this 8-module structure:

| Module | Topic | Hours |
|--------|-------|-------|
| 1 | Introduction to Computer Architecture and Organization | 5 |
| 2 | Data Representation and Computer Arithmetic | 5 |
| 3 | Instruction Sets and Control Unit | 9 |
| 4 | Memory System Organization and Architecture | 7 |
| 5 | Interfacing and Communication | 5 |
| 6 | Subsystems | 5 |
| 7 | High Performance Processors | 7 |
| 8 | Contemporary Issues | 2 |

**Primary textbook:** Patterson, Hennessy — *Computer Organization and Design: The Hardware/Software Interface* (6th ed., Morgan Kaufmann, 2020).

## Slide Conventions

- Use `format: revealjs` in the YAML front matter
- Use incremental bullet points for step-by-step explanations
- Include diagrams and block diagrams where possible for hardware concepts
- Use Quarto's built-in LaTeX math (`$...$` inline, `$$...$$` display) for address calculations, performance equations, and binary arithmetic
- Add speaker notes with `:::  {.notes}` blocks for lecture talking points

## File Layout

- `_quarto.yml` — project config with RevealJS defaults
- `theme.scss` — custom academic SCSS theme (teal palette, Source Sans Pro, callout classes)
- `lectures/` — module slide decks (`M1-intro-architecture.qmd` through `M8-contemporary.qmd`)
- `labs/` — lab session materials
- `assignments/` — homework and assignment files
- `docs/` — course documentation and handouts
- `images/` — shared diagrams and figures
- `reference/syllabus.pdf` — official syllabus (source of truth for topics and sequencing)
- `_output/` — rendered HTML output (gitignored)

### Custom CSS Classes (defined in `theme.scss`)

- `.theorem` — teal-bordered callout box for theorems and key principles
- `.definition` — gold-bordered callout box for definitions
- `.complexity` — inline badge for performance expressions (e.g., `[CPI = 1.5]{.complexity}`)
