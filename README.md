# QGS-Paper

This repository contains a short research paper / article analysis about **Samsung’s “Quantum Galaxy”** concept and how it can help secure smartphones using **Quantum Random Number Generation (QRNG)** and **Post-Quantum Cryptography (PQC)**.

The work is written in LaTeX using the **IEEEtran** format and analyzes the article:

**“Unveiling Samsung Quantum Galaxy: Securing Smartphones With Quantum and Post-Quantum Cryptography”**  
(published in **IEEE Access** on **May 2, 2025**)

## Repository contents

- `LaTeX Report/Relatorio.tex` — main LaTeX source (IEEEtran)
- `LaTeX Report/Relatorio.pdf` — compiled PDF output
- `LaTeX Report/Recursos/` — bibliography + assets (e.g., `.bib`, images)
- `Unveiling_Samsung_Quantum_Galaxy_Securing_Smartphones_With_Quantum_and_Post-Quantum_Cryptography.pdf` — a PDF copy of the referenced base paper (as included in this repo)
- `LICENSE` — repository license file

## What’s inside the paper

The report discusses, in a structured “article analysis” format:

- **Research problem & objectives:** securing modern smartphones against quantum threats while keeping compatibility with current crypto
- **Approach / methodology:** analysis of Samsung’s implementation + reverse engineering / forensics perspective as described by the base paper
- **QRNG quality discussion:** notes weaknesses found via statistical test suites (e.g., NIST SP800-22, Dieharder)
- **Role of PQC:** how post-quantum algorithms can mitigate future quantum attacks
- **Conclusions & contribution:** feasibility of combining QRNG + PQC on consumer devices

## Quick access

- **Compiled report:** `LaTeX Report/Relatorio.pdf`
- **LaTeX source:** `LaTeX Report/Relatorio.tex`
- **Referenced paper (PDF):** `Unveiling_Samsung_Quantum_Galaxy_Securing_Smartphones_With_Quantum_and_Post-Quantum_Cryptography.pdf`

## Build the PDF (LaTeX)

### Option A — latexmk (recommended)

```bash
cd "LaTeX Report"
latexmk -pdf -interaction=nonstopmode -shell-escape Relatorio.tex
```

### Option B — pdflatex + biber

```bash
cd "LaTeX Report"
pdflatex Relatorio.tex
biber Relatorio
pdflatex Relatorio.tex
pdflatex Relatorio.tex
```

> Note: The project uses `biblatex` with `backend=biber`, so `biber` is required to generate the references.

## Notes

This repo contains LaTeX build artifacts (e.g., `.aux`, `.log`, `.bcf`, etc.) committed alongside the source. If you want, I can also propose a `.gitignore` for a cleaner structure.

## Authors

- Martinho José Novo Caeiro
- Paulo António Tavares Abade

## License

See `LICENSE`.
