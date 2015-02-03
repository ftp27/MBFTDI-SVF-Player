CC=gcc

LIBPATH = /Users/ftp27/gitclones/fidi/build/x86_64
INCPATH = /Users/ftp27/gitclones/fidi/

OFLAGS = -g -O3
SFLAG1 = -std=c99
SFLAG2 = -m64
SFLAGS = $(SFLAG1) $(SFLAG2)

CFLAGS  =-ldl -lpthread
CFLAGS += $(LIBPATH)/libftd2xx.a
CFLAGS += -I../common
CFLAGS += -I$(INCPATH)
CFLAGS += -D _MAC
CFLAGS += $(SFLAGS) $(OFLAGS) 

APP = mbftdi
all: $(APP)

$(APP): mbftdi.c ../common/mblastercore.c
	$(CC) mbftdi.c ../common/mblastercore.c -o $(APP) $(CFLAGS)

clean:
	rm -f *.o ; rm $(APP)
