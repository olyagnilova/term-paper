# makefile: tex -> pdf

file_name = paper

$(file_name).pdf: $(file_name).tex
	# protection against biber error
	# http://tex.stackexchange.com/questions/140814/
	rm -rf `biber --cache`

	# create pdf
	# will automatically run pdflatex/biber if necessary
	latexmk -xelatex $(file_name).tex

	# clean auxillary files
	latexmk -c $(file_name).tex

clean:
	-rm $(file_name).log $(file_name).aux $(file_name).bbl $(file_name).bcf $(file_name).blg $(file_name).fdb_latexmk $(file_name).fls $(file_name).out $(file_name).run.xml $(file_name).xdv
