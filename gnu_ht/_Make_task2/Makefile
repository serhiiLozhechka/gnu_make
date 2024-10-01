# Define variables
MAIN_OBJ = main.o
OBJ1 = src1.o
OBJ2 = src2.o
OBJ3 = src3.o
EXE = program

# If USE_INCLUDE is set to true, include the .mk files
ifeq ($(USE_INCLUDE), true)
    include make1.mk
    include make2.mk
    include make3.mk
endif

# Rule to build the main object file
$(MAIN_OBJ): main.c
	@echo "Compiling main.c into main.o"
	gcc -c main.c -o $(MAIN_OBJ)

# Rule to build the final executable
all: $(MAIN_OBJ) $(OBJ1) $(OBJ2) $(OBJ3)
	@echo "Linking all object files into $(EXE)"
	gcc $(MAIN_OBJ) $(OBJ1) $(OBJ2) $(OBJ3) -o $(EXE)

# Clean up object files and executable
clean:
	rm -f $(MAIN_OBJ) $(OBJ1) $(OBJ2) $(OBJ3) $(EXE)
