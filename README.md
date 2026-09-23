# A pdf of my resume (shown below) can be downloading by clicking [here](build/test-resume.pdf) and using the "Download Raw File" option.

<img width="611" height="791" alt="image" src="https://github.com/user-attachments/assets/cae41ce8-8065-4e05-888c-061224d014b6" />


# ATS-Optimized Latex Resume Template

The main resume source file to edit is
[`resume.tex`](resume.tex). Follow the instructions below to view your edits in vscode. The custom document class is in
[`resume.cls`](resume.cls).

## VS Code setup (Recommended)

1. Install a LaTeX distribution that includes `pdflatex` and `latexmk`.
   On Ubuntu/WSL:

   ```bash
   sudo apt update
   sudo apt install latexmk texlive-latex-extra texlive-extra-utils
   ```

2. Open this folder in VS Code. Install the recommended **LaTeX Workshop**
   extension when prompted.
3. Open `resume.tex`. LaTeX Workshop will build on save and open the PDF in a
   VS Code tab. You can also run **LaTeX Workshop: Build LaTeX project** from
   the Command Palette.

The generated PDF and intermediate files are written to `build/`.

## Command-line build

After installing the LaTeX tools, run:

```bash
latexmk -pdf -interaction=nonstopmode -synctex=1 -file-line-error \
  -outdir=build resume.tex
```

The exported file will be `build/resume.pdf`.

To remove generated files:

```bash
latexmk -C -outdir=build resume.tex
```
