.SUFFIXES: .erl .beam .hrl

INCLUDE = ../include

OUTPUT = ../ebin

MODULES = test cdrv_app cdrv_sup cdrv

all: compile

compile: $(OUTPUT) $(MODULES:%=$(OUTPUT)/%.beam)

edoc: $(DOCDIR) $(MODULES:%=$(DOCDIR)/%.html)

$(OUTPUT)/%.beam:%.erl
	erlc +debug_info -o $(OUTPUT) -I $(INCLUDE) -W $<

$(OUTPUT):
	mkdir $(OUTPUT)

clean:
	rm -rf $(OUTPUT)/*.beam $(DOCDIR) *~
