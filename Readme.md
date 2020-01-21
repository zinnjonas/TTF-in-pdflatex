# Description

This bash skrip creates the files needed by pdflatex to include a font into the document.
The placles the skript will copy the files are configured for an Arch linux.
This may need adjustment for different distrubutions / Texlive installations.

# How To Use

Create a folder with the name of the font to install.
With sup-folders: rm, sf and tt.
Place in the rm folder the font you want to use for the roman font style.
In sf the Sans font and in tt the monospaced version.

If you leave one or more folders empty there wont be a problem.

Execute the skript in the Font-Folder. (Currently it uses sudo rights)

After the skript run successfully the font can be used in (La)TeX as default font with:

```latex
\renewcommand{\rmdefault}{FONTNAME_rm}
\renewcommand{\sfdefault}{FONTNAME_sf}
\renewcommand{\ttdefault}{FONTNAME_tt}
```

or for a small supset of the document:

```latex
{\fontfamily{FONTNAME_rm}\selectfont Some Text}
```

Where `FONTNAME` is the name of the font-folder. 


