TEX = xelatex
BIB = bibtex

src = 2020-GS-ARTICLE.tex
bcf = 2020-GS-ARTICLE

PDF = 2020-GS-ARTICLE.pdf
WCN = pdftotext 2020-GS-ARTICLE.pdf - | wc -c > includes/char.txt
CCN = pdftotext 2020-GS-ARTICLE.pdf - | wc -w > includes/words.txt

publish :
	$(TEX) $(src) && $(BIB) $(bcf) && $(TEX) $(src) && $(TEX) $(src) && $(WCN) && $(CCN) && $(TEX) $(src) && rm *.aux *.log *.bbl *.blg *.out

build :
	$(TEX) $(src) && $(BIB) $(bcf) && $(TEX) $(src) && $(TEX) $(src) && $(WCN) && $(CCN) && $(TEX) $(src)

step :
	$(TEX) $(src)

.PHONY: clean
clean :
	rm *.aux *.log *.toc *.run.xml *.bbl *.blg *.bcf *.fdb_latexmk *.fls *.idx *.ilg *.ind *.lof *.lot *.pdf *.out
