CFLAGS = -g

CFLAGS += -MMD -MT $@ -MF $@.d

OBJ = $(patsubst %.c,%.o,$(wildcard *.c)) $(patsubst %.S,%.o,$(wildcard *.S))

all : main

main : $(OBJ)
	$(CC) $^ -o $@

clean :
	rm -f *.o *.d main $(APPS)

-include $(patsubst %,%.d,$(OBJ))
