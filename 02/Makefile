CC=g++
CFLAGS= -c -std=c++11 -march=native -g3 -Wall -O0
LDFLAGS= -g3

SOURCES=lodepng.cc mandelbrot1a.cc mandelbrot1b.cc
HEADERS=lodepng.h complex.h

EXECUTABLES=mandelbrot1a mandelbrot1b

OBJECTS=$(SOURCES:.cc=.o)

all: $(EXECUTABLES)

mandelbrot1a: lodepng.o mandelbrot1a.o
	$(CC) $(LDFLAGS) lodepng.o mandelbrot1a.o -o $@

mandelbrot1b: lodepng.o mandelbrot1b.o
	$(CC) $(LDFLAGS) lodepng.o mandelbrot1b.o -o $@

%.o: %.cc
	$(CC) $(CFLAGS) $< -o $@

clean:
	$(RM) $(OBJECTS) $(EXECUTABLES)
