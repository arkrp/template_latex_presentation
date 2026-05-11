TOPTARGETS := run clean

project_directory=$(shell pwd)
export project_directory

run: pdf/paper.pdf
	zathura pdf/paper.pdf

pdf/paper.pdf: paper.tex refs.bib pdf $(SUBDIRS)
	latexmk -pdf -output-directory="./pdf" paper

pdf:
	mkdir pdf

clean:
	-rm -rf pdf
	-rm -rf venv

.PHONY: $(TOPTARGETS)
