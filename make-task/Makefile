CC      = gcc
CFLAGS  = -Wall -Wextra -Iinclude

TARGET  = calculator
OBJS    = main.o calculator.o logger.o

all: $(TARGET)

$(TARGET): $(OBJS)
	$(CC) $(OBJS) -o $(TARGET)

main.o: src/main.c include/calculator.h include/logger.h
	$(CC) $(CFLAGS) -c src/main.c -o main.o

calculator.o: src/calculator.c include/calculator.h
	$(CC) $(CFLAGS) -c src/calculator.c -o calculator.o

logger.o: src/logger.c include/logger.h
	$(CC) $(CFLAGS) -c src/logger.c -o logger.o

.PHONY: all clean

clean:
	rm -f $(TARGET) $(OBJS)