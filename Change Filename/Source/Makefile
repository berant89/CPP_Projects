#Directories.
ODIR = obj
SOURCE = Source
IDIR = ../Include
#Compiler to use.
CC=g++
EXT = cpp
#Options to pass to the compiler.
CFLAGS=-I$(IDIR) -Wall

_DEPS = alphanum.h alphanum_old.h FileManip.h mergesort.h quicksort.h
DEPS = $(patsubst %,$(IDIR)/%,$(_DEPS))
_OBJ = alphanum.o alphanum_old.o FileManip.o mergesort.o quicksort.o
OBJ = $(patsubst %,$(ODIR)/%,$(_OBJ))

$(ODIR)/%.o: %.$(EXT) $(DEPS)
	$(CC) -c $(CFLAGS) $< -o $@

.PHONY: all
all: change_name

change_name: $(OBJ)
	$(CC) $(CFLAGS) $^ -o $@

.PHONY: clean

clean:
	rm -vf $(ODIR)/*.o *~
