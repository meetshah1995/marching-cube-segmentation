CC=g++

OPENGLLIB= -framework OpenGL
GLEWLIB= -lGLEW
GLFWLIB = -lglfw3
LIBS=$(OPENGLLIB) $(GLEWLIB) $(GLFWLIB)
LDFLAGS=-L/usr/local/lib
CPPFLAGS=-I/usr/local/include -I./

BIN=application.out
SRCS=application.cpp gl_framework.cpp shader_util.cpp
INCLUDES=gl_framework.hpp shader_util.hpp application.hpp

.phony: all clean algo

all: $(BIN)

$(BIN): $(SRCS) $(INCLUDES)
	g++ $(CPPFLAGS) $(SRCS) -o $(BIN) $(LDFLAGS) $(LIBS)

clean:
	rm -f *~ *.o $(BIN)

algo:
	cd algorithm; make; ./marching_cube.out

unit:
	cd algorithm; make unit; ./unit_bin.out

prman:
	cd renderman; make;