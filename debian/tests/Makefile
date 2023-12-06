TESTS=readogg

all: $(TESTS) $(TESTS:%=%_test)
clean:
	@rm -f $(TESTS) $(TESTS:%=%_test)

.PHONY: all clean

CFLAGS=$(shell pkg-config --cflags ogg)
LDLIBS=$(shell pkg-config --libs ogg)
infile=test.ogg

%_test: %

readogg_test: readogg
	cat $(infile) | ./$^
