CC=mpicxx
include=-I common -I ./omp-tasks/alignment/alignment_for

all:botsalgn
botsalgn:bots_main.o bots_common.o alignment.o
	${CC} -o botsalgn -fopenmp bots_main.o bots_common.o alignment.o
bots_main.o:
	${CC} -o bots_main.o -fopenmp -c ${include} common/bots_main.c
bots_common.o:
	${CC} -o bots_common.o -fopenmp -c ${include} common/bots_common.c
alignment.o:
	${CC} -o alignment.o -fopenmp -c ${include} ./omp-tasks/alignment/alignment_for/alignment.c
clean:
	rm -f botsalgn *.o