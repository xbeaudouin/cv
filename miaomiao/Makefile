CVNAME?=mbeaudouin
CVTHEME?=sharp
LATEX=xelatex

export TEXINPUTS=.:../../cv4tw:
#export TTFONTS = .;$TEXMF/fonts/{truetype,opentype}//;$OSFONTDIR//
#export OPENTYPEFONTS = .;$TEXMF/fonts/{opentype,truetype}//;$OSFONTDIR//

all: $(CVNAME)-$(CVTHEME).pdf
	mv $(CVNAME)-$(CVTHEME).pdf $(CVNAME).pdf
	make proper

force: clean all

clean: proper
	rm -f $(CVNAME)-$(CVTHEME).pdf

proper:
	rm -f $(CVNAME)-$(CVTHEME).log $(CVNAME)-$(CVTHEME).out $(CVNAME)-$(CVTHEME).aux missfont.log

$(CVNAME)-$(CVTHEME).pdf: $(CVNAME)-$(CVTHEME).tex
	@$(LATEX) $<
	#run it twice, to fix page numbers
	@$(LATEX) $<
