
LIBNAME	:= luadq.so

OBJS		:= luadq.o

CFLAGS	:= -O3 -fPIC -W -Wall -Wextra -pedantic -ansi -Wconversion -Wunused -Wshadow -Wpointer-arith -Wmissing-prototypes -Winline -Wcast-align -Wmissing-declarations -Wredundant-decls -Wno-long-long -Wcast-align
#CFLAGS	:= -g -DDQ_CHECK -fPIC -W -Wall -Wextra -Werror -pedantic -ansi
CFLAGS   += $(shell pkg-config lua --cflags)
LDFLAGS	:= -ldq



.PHONY: all clean


all: $(LIBNAME)

$(LIBNAME): $(OBJS)
	$(CC) -shared -o $(LIBNAME) -shared $(OBJS) $(LDFLAGS)

clean:
	$(RM) $(OBJS) $(LIBNAME)

