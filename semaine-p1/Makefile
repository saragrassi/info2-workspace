SOURCES=$(wildcard *.c)
EXECS=$(patsubst %.c,%,$(SOURCES))
CC = gcc
CCFLAGS=-std=c17 -g -Wall  -pedantic -Werror
LDFLAGS=-lm

all: build

build: $(EXECS)

%: %.c
	$(CC) $(CCFLAGS) $? -o $@ $(LDFLAGS)

clean:
	rm -f $(EXECS) a.out

.PHONY: all  build

# first target $@
# all prerequisites newer than the target $?
# all prerequisites $^
