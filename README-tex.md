## Requirements
- sudo apt-get install asciidoctor
- sudo apt-get install texlive-xetex

## Steps

Convert to docbook format

`asciidoctor -b docbook5 ./btcphilosophy.adoc`

Convert to LaTeX format

`pandoc -f docbook btcphilosophy.xml --pdf-engine=xelatex -o btcphilosophy.tex`

Paste .tex file inside LaTeX template


## Post

Sections -> Chapters
Subsection -> Sections

Getting hrefs:

`sed -n -e 's/.*\\href{\([^}]*\)}.*/\1/p' btcphilosophy.tex > links.txt`

