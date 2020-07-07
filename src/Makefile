TARGET = badger-trap
OLDTARGET = badger-trap-v3
SRC = badger-trap.c

CC = gcc
CFLAGS = -Wall

.PHONY: default all clean

default: $(TARGET)
all: default $(OLDTARGET)

$(TARGET): $(SRC)
	$(CC) $(CFLAGS) -DBADGERTRAP_SYSCALL_NO=335 $< -o $@

$(OLDTARGET): $(SRC)
	$(CC) $(CFLAGS) -DBADGERTRAP_SYSCALL_NO=314 $< -o $@

distclean:
	-rm -f $(TARGET) $(OLDTARGET)
