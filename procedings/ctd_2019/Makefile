# -----------------------------------------
# Makefile for cover letter, cv, research statement and list of publications
# -----------------------------------------
TEXFILE = eprint

TEX=pdflatex
BIBTEX=bibtex

SOURCES         = $(wildcard ./*.tex)
BIBFILE         = $(widlcard ./*.bbl)
EPSFIGURES      = $(wildcard figures/*.eps)

all: ${TEXFILE}.pdf

${TEXFILE}.bbl: ${TEXFILE}.bib
	$(BIBTEX) ${TEXFILE}

${TEXFILE}.pdf: ${SOURCES} ${EPSFIGURES} ${BIBFILE}
	$(TEX) ${TEXFILE}.tex
	$(TEX) ${TEXFILE}.tex && $(TEX) ${TEXFILE}.tex 

clean:
	rm -f ${TEXFILE}.ps ${TEXFILE}.dvi ${TEXFILE}.aux *.log ${TEXFILE}.pdf ${TEXFILE}.bbl *.out *.toc ${TEXFILE}.blg *~
