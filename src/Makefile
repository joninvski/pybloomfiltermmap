CC = gcc
CFLAGS = -lm -g

all: bloomfilter mbarray

bloomfilter: mmapbitarray.* bloomfilter.*
	$(CC) $(CFLAGS)  mmapbitarray.c bloomfilter.c -o bf

mbarray: mmapbitarray.*
	$(CC) $(CFLAGS)	-DMBAQUERY mmapbitarray.c -o mbaquery
	$(CC) $(CFLAGS) -DMBACREATE mmapbitarray.c -o mbacreate

clean:
	rm ./mbaquery ./mbacreate ./bf
