CC=gcc
CFLAGS=-Wall -g
OFLAGS=-O3 -fopenmp
AFLAGS=-march=native -mtune=native
LFLAGS=-lm

all: dotprod_parallel dotprod_parallel_atomic dotprod_parallel_simd

dotprod_parallel: dotprod_parallel.c
	$(CC) $(AFLAGS) $(CFLAGS) $(OFLAGS) $< -o $@ $(LFLAGS) 

dotprod_parallel_atomic: dotprod_parallel_atomic.c
	$(CC) $(AFLAGS) $(CFLAGS) $(OFLAGS) $< -o $@ $(LFLAGS) 

dotprod_parallel_simd: dotprod_parallel_simd.c
	$(CC) $(AFLAGS) $(CFLAGS) $(OFLAGS) $< -o $@ $(LFLAGS) 

clean:
	rm -Rf dotprod_parallel dotprod_parallel_atomic dotprod_parallel_simd
