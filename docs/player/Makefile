.SUFFIXES:
.SUFFIXES: .md .frag.html .html

MARKDOWN=~/Applications/Markdown/Markdown_1.0.1/Markdown.pl

MD_FILES = $(wildcard *.md)
HFRAG_FILES = $(MD_FILES:.md=.frag.html)
HTML_FILES = $(MD_FILES:.md=.html)

TEMPLATE_HTML_FILES= head.templ.html foot.templ.html

.md.frag.html:
	$(MARKDOWN) $< > $@

.frag.html.html:
	cat head.templ.html $< foot.templ.html | sed "s/HTML_TITLE/$(basename $@)/" > $@

all: $(HTML_FILES)

clean:
	-rm $(HTML_FILES)
