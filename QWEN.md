# McMaster University Thesis - QWEN Context

## Project Overview

This is a **LaTeX thesis project** for McMaster University's School of Graduate Studies, focusing on **"Optical Character Recognition to Image Generation"**. The thesis explores the integration of OCR technology, natural language processing, and AI-driven image generation to transform textual content into visual representations.

**Author:** Yuan Gao  
**Degree:** Master of Engineering  
**Department:** Computing and Software  
**Expected Submission:** February 2025  
**Supervisor:** Dr. Yingying Wang

## Project Structure

### Core Files
- **`Thesis_Main.tex`** - Main thesis document that includes all chapters and manages the overall structure
- **`definitions.tex`** - Contains all thesis metadata (author info, department, degree details, dates)
- **`notation.tex`** - Defines abbreviations, definitions, and notation used throughout the thesis
- **`gscale_thesis_doublespace.sty`** - McMaster SGS formatting style file for double-spaced thesis (compliant with 2021 guidelines)
- **`chapter4_new_citations.bib`** - Bibliography file with recent citations for Chapter 4 (OCR section)

### Directory Structure
- **`chapters_before_preface/`** - Preliminary pages (abstract, dedication, acknowledgements, declaration)
- **`chapters_after_preface/`** - Main thesis chapters (introduction, background, system overview, OCR, etc.)
- **`chapters_after_preface_appendix/`** - Appendix sections
- **`figures/`** - Thesis figures and diagrams
- **`references/`** - Bibliography files (`references_first.bib`, `references_another.bib`)
- **`guideline_and_sample_thesis/`** - McMaster SGS guidelines and sample materials

## Thesis Chapters

1. **Introduction** - Problem statement, motivation, and research objectives
2. **Background** - Literature review and theoretical foundation
3. **System Overview** - High-level system architecture and design
4. **OCR** - Optical Character Recognition implementation and optimization
5. **AbstractGen** - Abstract generation component
6. **TextGenImage** - Text-to-image generation system
7. **Results** - Experimental results and evaluation
8. **Conclusion** - Summary and future work

## Technical Requirements

### LaTeX Configuration
- **Compiler:** pdfLaTeX
- **TeX Live Version:** 2020 (Legacy compatibility)
- **Document Class:** `report` with letterpaper, 12pt
- **Spacing:** Double-spaced (compliant with McMaster SGS requirements)

### Key Packages
- **Bibliography:** `natbib` with `abbrvnat` style
- **Figures:** `graphicx`, `subcaption`, `float`
- **Tables:** `booktabs`, `longtable`, `tabularx`
- **Mathematics:** `amsmath`, `amsfonts`
- **Diagrams:** `tikz`, `pgfplots`
- **Code Highlighting:** `minted`, `listings`
- **Hyperlinks:** `hyperref` with hidelinks option

## Building and Compilation

### Standard Build Process
```bash
# Compile the main thesis document
pdflatex Thesis_Main.tex

# Generate bibliography
bibtex Thesis_Main

# Final compilation (run multiple times for references)
pdflatex Thesis_Main.tex
pdflatex Thesis_Main.tex
```

### Using minted Package (Code Highlighting)
The thesis uses the `minted` package for code highlighting, which requires:
- Python with Pygments installed: `pip install Pygments`
- Shell escape enabled: `pdflatex -shell-escape Thesis_Main.tex`

## Development Guidelines

### File Organization
- Each chapter is a separate `.tex` file in the appropriate directory
- Figures are stored in the `figures/` directory with descriptive names
- Bibliography entries are distributed across multiple `.bib` files for organization
- Custom commands and definitions go in `definitions.tex`

### Formatting Standards
- **Margins:** 0.5in left/right, 0.5in header separation
- **Text:** 6in width, 8.1in height
- **Font:** Times New Roman equivalent, 12pt
- **Line Spacing:** Double-spaced (1.5 in LaTeX baselinestretch)
- **Page Numbers:** Follow McMaster SGS guidelines

### Citation Style
- Uses `natbib` package with numerical citations in IEEE format
- Bibliography style: `IEEEtran` (IEEE Transactions format)
- Numerical citations in square brackets [1], [2], etc.
- Recent citations include 2024-2025 publications on OCR and AI
- All bibliography entries follow IEEE standards

## Research Focus Areas

### OCR Enhancement
- Custom Tesseract OCR model training
- Image preprocessing techniques for improved accuracy
- Handling of handwritten content and low-quality images

### Natural Language Processing
- Local deployment of GPT-OSS-20B (21 billion parameters)
- Prompt engineering for text-to-image transformation
- Error correction and semantic enhancement

### Image Generation
- Integration with FLUX 1.1 Pro Ultra diffusion models
- Multimodal AI system architecture
- Privacy-preserving local deployment

## Common Tasks

### Adding New Chapters
1. Create a new `.tex` file in `chapters_after_preface/`
2. Add the include statement in `Thesis_Main.tex` after the appropriate section
3. Reset counters for figures, equations, and tables

### Adding Figures
1. Place figure files in the `figures/` directory
2. Use descriptive filenames (e.g., `ocr_pipeline_diagram.png`)
3. Include using `\includegraphics` with appropriate scaling

### Updating Bibliography
1. Add new citations to the appropriate `.bib` file
2. Use consistent citation keys following the existing pattern
3. Ensure all required fields are present for the publication type

## Troubleshooting

### Common Issues
- **minted compilation errors:** Ensure Pygments is installed and shell escape is enabled
- **Bibliography not showing:** Run bibtex and recompile multiple times
- **Formatting issues:** Check that `gscale_thesis_doublespace.sty` is being used
- **Hyperlink colors:** Set to hidden (hidelinks option) for professional appearance

### Overleaf Compatibility
The template is designed to be compatible with Overleaf, with all required packages included in the preamble.