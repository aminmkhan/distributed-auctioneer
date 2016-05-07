# ---------------------------------------------------------
# type "make" command in Unix to create the PDF file 
# ---------------------------------------------------------

# Main filename
FILE=main

# ---------------------------------------------------------

all:
	pdflatex  ${FILE} -interaction=nonstopmode -synctex=1
# 	makeindex $(FILE).nlo -s nomencl.ist -o $(FILE).nls
# 	makeindex $(FILE).glo -s $(FILE).ist -o $(FILE).gls -t $(FILE).glg
	bibtex ${FILE}
	pdflatex  ${FILE} -interaction=nonstopmode -synctex=1
	pdflatex  ${FILE} -interaction=nonstopmode -synctex=1

once:
	pdflatex  ${FILE} -interaction=nonstopmode -synctex=1
	
clean:
	(rm -rf *.aux *.bbl *.blg *.glg *.glo *.gls *.ilg *.ist *.lof *.log *.lot *.nlo *.nls *.out *.toc *.bcf *.tdo *.run.xml *.synctex.gz)

veryclean:
	make clean
	rm -f *~ *.*%
	rm -f $(FILE).pdf $(FILE).ps

