SRC=deviant.cpp individu.cpp personne.cpp main.cpp tests.cpp
EXE=examen
CXX=g++
CXXFLAGS+=-Wall -Wextra -MMD -g
LDFLAGS=

OBJ=$(addprefix build/,$(SRC:.cpp=.o))
DEP=$(addprefix build/,$(SRC:.cpp=.d))

all: $(OBJ)
	$(CXX) -o $(EXE) $^ $(LDFLAGS)

build/%.o: %.cpp
	@mkdir -p build
	$(CXX) $(CXXFLAGS) -o $@ -c $<

clean:
	rm -rf build core *.gch

-include $(DEP)
