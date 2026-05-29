# Keqing Liu - Personal Homepage

This repository contains the source code for my personal website hosted via GitHub Pages.

Website:  
https://keqing-liu.github.io

## About

This website presents information about:

- Research
- Teaching
- Policy reports
- Curriculum vitae (CV)

The website is designed as a lightweight academic homepage using static HTML and CSS.

## Repository Structure

```text
.
├── index.html          # Main homepage
├── research.html       # Research and publications
├── teaching.html       # Teaching experience and course materials
├── policy.html         # Policy reports and related work
├── aboutme.html        # Additional personal information
│
├── images/             # Profile photo and website images
├── files/              # Public paper PDFs and related downloadable files
├── cv/                 # CV source files and compiled PDFs
│   ├── cv_academic.tex
│   ├── cv_academic.pdf
│   ├── cv_industry.tex
│   └── cv_industry.pdf
│
├── README.md
└── .gitignore
```

## CV Workflow

The CV files are maintained in `cv/`.

- `cv_academic.tex` generates the academic CV.
- `cv_industry.tex` generates the industry CV.
- The compiled PDFs are kept in the same folder so the website can link directly to them.

To compile a CV locally:

```bash
cd cv
latexmk -pdf cv_academic.tex
latexmk -pdf cv_industry.tex
latexmk -c
```

The cleanup command removes LaTeX intermediate files. These generated files are also ignored by `.gitignore`.

## Private Materials

The `private/` folder is intended for local job application materials, such as cover letter drafts, job descriptions, and application notes. It is excluded from version control through `.gitignore` and should not be committed to the public website repository.

## Deployment

The site is deployed through GitHub Pages from the static files in this repository.
