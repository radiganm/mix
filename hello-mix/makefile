#!/usr/bin/make
## makefile (for hello.mix)
## Mac Radigan

target = hello

.SUFFIXES: .mix .mixal

.PHONY: default build run clean

CC = mixasm

SRC = \
  $(target).mix \
  goodbye.mix


default: $(target)

build: $(SRC)

$(target): build
	mixvm -r $(target).mix

%.mix : %.mixal
	$(CC) $< -o $@

clean:
	-rm ./*.mix

## *EOF*
