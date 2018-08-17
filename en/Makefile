export TEXINPUTS=../tex//:

all: autoreferat_thesis-summary.pdf

# LaTeX must be run multiple times to get references right
thesis.pdf: thesis.tex $(wildcard *.tex) bibliography.bib thesis.xmpdata
	pdflatex $<
	bibtex thesis
	pdflatex $<
	pdflatex $<

autoreferat_thesis-summary.pdf: autoreferat_thesis-summary.tex $(wildcard *.tex) bibliography.bib thesis.xmpdata
	pdflatex $<
	bibtex thesis
	pdflatex $<
	pdflatex $<
clean:
	rm -f *.log *.dvi *.aux *.toc *.lof *.lot *.out *.bbl *.blg *.xmpi
	rm -f thesis.pdf
