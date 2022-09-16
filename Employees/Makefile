# Name: Ethan Buchanan
# File: Makefile
# Date: 9/15/22


CC = g++
TARGET = employee
CFLAGS = -g -Wall -Wextra
# Complies showing all errors and warnings

all: employee

# List the object files needed to create the executable file.

$(TARGET):	Employee.o main.o Supervisor.o Officer.o
	$(CC) $(CFlags) -o $(TARGET) main.o Employee.o Supervisor.o Officer.o

# Creates the rules need to link everything to main

main.o: main.cpp Employee.h Supervisor.h Officer.h
	$(CC) $(CFLAGS) -c main.cpp

# Creates the rules for Employee.o

Employee.o:	Employee.cpp Employee.h
	$(CC) $(CFLAGS) -c Employee.cpp

# Creates the rules for Supervisor.o

Supervisor.o:     Supervisor.cpp Supervisor.h
	$(CC) $(CFLAGS) -c Supervisor.cpp

# Creates the rules for Officer.o
Officer.o:     Officer.cpp Officer.h
	$(CC) $(CFLAGS) -c Officer.cpp

# Creates a blank slate (done by 'make clean')

clean:
	$(RM) employee *.o *~
