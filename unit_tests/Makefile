VERSION  := 1.0.0.0
GIT_VERSION := $(shell git log --format="%h" -n 1)

CPP = g++

CFLAGS = -Wall -Wno-write-strings -DVERSION=\"$(VERSION)\" -DGIT_VERSION=\"$(GIT_VERSION)\"
LIBS = -lgtest -lpthread

# Define DEBUG
ifdef DEBUG
	CFLAGS += -g -DDEBUG
else
	CFLAGS += -O3
endif

APP = avltreeTest
SRC =   ../avltree.c \
		UnitTest_avltree.c \
		UnitTest_Google.c
all:
	$(CPP) -o $(APP) $(SRC) $(CFLAGS) $(LIBS)

test:
	./$(APP)