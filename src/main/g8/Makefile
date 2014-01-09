SRC_DIR = src
DEST_DIR = target
SRC_MAIN = $(SRC_DIR)/main
DEST_MAIN = $(DEST_DIR)/main

all: pdf bib idx

pdf:
	mkdir -p $(DEST_DIR)
	pdflatex -output-directory=$(DEST_DIR) -file-line-error -interaction=nonstopmode -synctex=1 -etex $(SRC_MAIN)

bib:
	bibtex8 $(DEST_MAIN)

idx:
	makeindex $(DEST_MAIN)

clean:
	rm -rf $(DEST_DIR)
