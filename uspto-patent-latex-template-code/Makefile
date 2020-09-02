drawings.pdf: drawings.ps
	ps2pdf drawings.ps drawings.pdf

%.pdf: %.ps
	ps2pdf $*.ps $*.pdf

clean:
	rm -rf $(input) $(output)
	rm -rf *.log *.aux *.bbl *.blg


%.ps: %.dvi
	dvips -f $*.dvi > $*.ps

%.dvi: %.tex
	-latex -interaction=nonstopmode $*.tex
	latex $*.tex
	-bibtex $*
	latex $*.tex
