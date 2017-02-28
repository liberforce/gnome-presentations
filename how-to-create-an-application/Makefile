.PHONY: all clean
OBJS=how-to-create-an-application.pdf
DOC=$*.tmp

all: ${OBJS}

%.pdf: %.pin
	@grep -v '^#' $< > ${DOC} # Remove comments from the generated pdf
	@cat CREDITS >> ${DOC}    # Append credits
	pinpoint ${DOC} -o $@
	-rm ${DOC}

clean:
	-rm ${OBJS}
