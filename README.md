# Resume of Md. Mosfikur Rahman

This repository contains the LaTeX source files for my resume, along with a GitHub Actions workflow for automatically building and deploying the PDF version.

## Files

- **index.html**: Redirects to the latest PDF version of the resume.
- **Resume-Mosfik.tex**: The LaTeX source file for the resume.
- **Makefile**: Automates the process of compiling the LaTeX file to PDF.
- **.github/workflows/build.yml**: GitHub Actions workflow for building and deploying the PDF.

## Usage

### Build Locally

To build the resume PDF locally, you'll need to have a LaTeX distribution installed. Run the following command:

```bash
make all
```

This will generate `Resume-Mosfik.pdf`.

### Clean

To remove all generated files, use:

```bash
make clean
```

To also remove the PDF:

```bash
make distclean
```

## GitHub Actions

The repository includes a GitHub Actions workflow (`.github/workflows/build.yml`) that automatically builds the PDF from the LaTeX source and deploys it to the `build` branch. The following steps are performed:

1. **Build**:
    - Checks out the repository.
    - Compiles the LaTeX file into a PDF using `latexmk`.
    - Uploads the PDF as an artifact.

2. **Deploy**:
    - Downloads the PDF artifact.
    - Deploys the PDF to the `build` branch using `gh-pages`.

3. **Copy index.html**:
    - Copies the `index.html` file to the `build` branch to ensure the latest resume PDF is accessible.

## Accessing the Resume

The resume can be accessed via the `index.html` file, which automatically redirects to the latest PDF version (`Resume-Mosfik.pdf`).

