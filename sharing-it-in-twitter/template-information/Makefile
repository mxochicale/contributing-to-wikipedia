INKSCAPE?=inkscape	# Inkscape (svg support)

FIGURES_SVG=$(wildcard vectorfiles/*.svg)
FIGURES_PNG=$(subst vectorfiles/,versions/,$(FIGURES_SVG:.svg=.png))

all:	$(FIGURES_PNG)

# Pattern rule for converting SVG to PNG
versions/%.png: vectorfiles/%.svg
	$(INKSCAPE) --export-png $(@) $(<)

viewpng:
	eog $(FIGURES_PNG)

clean:  ## Clean LaTeX and output figure files
	rm -f $(FIGURES_PNG)

