# Minimal makefile for Sphinx documentation
#

# You can set these variables from the command line.
DOCS        = docs
PYTHON      = python3
SPHINXOPTS  =
SPHINXBUILD =  -msphinx
SPHINXPROJ  = ReFrame
SOURCEDIR   = .
RM          = /bin/rm -rf

TARGET_DOCS := \
	help \
	html \
	dirhtml \
	singlehtml \
	pickle \
	json \
	htmlhelp \
	qthelp \
	devhelp \
	epub \
	latex \
	latexpdf \
	latexpdfja \
	text \
	man \
	textinfo \
	info \
	gettext \
	changes \
	xml \
	pseudoxml \
	linkcheck \
	doctest \
	coverage

latest:
	@make html
	@make man && mkdir -p man/man1 man/man8 && \
		mv man/reframe.1 man/man1/ && mv man/reframe.settings.8 man/man8/
	@touch html/.nojekyll

clean:
	@echo 'Removing directories'
	-$(RM) $(TARGET_DOCS) doctrees

$(TARGET_DOCS): Makefile
	@$(PYTHON) $(SPHINXBUILD) -M $@ "$(SOURCEDIR)" "" $(SPHINXOPTS) $(O)



.PHONY: clean latest Makefile
