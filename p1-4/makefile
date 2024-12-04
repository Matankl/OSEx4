# Compiler and Flags
CXX = g++
CXXFLAGS = -std=c++17 -Wall -pg
CCOVFLAGS = -g -fprofile-arcs -ftest-coverage -Og

# Files
SRC = mainRandom.cpp graph_and_Euler.cpp Graph.hpp
TARGET = mainRandom

# Default target: Compile the program
all: mainRandom

mainRandom: mainRandom.o graph_and_Euler.o
	g++ $(CXXFLAGS) $(CCOVFLAGS) -o $(TARGET) mainRandom.o graph_and_Euler.o

#init .o files
mainRandom.o: mainRandom.cpp graph_and_Euler.cpp Graph.hpp
	g++ $(CXXFLAGS) $(CCOVFLAGS) -c mainRandom.cpp graph_and_Euler.cpp

graph_and_Euler.o: graph_and_Euler.cpp Graph.hpp
	g++ $(CXXFLAGS) $(CCOVFLAGS) -c graph_and_Euler.cpp

# Clean build files
clean:
	rm -f mainRandom  *.gcda *.gcno *.o gmon.out
