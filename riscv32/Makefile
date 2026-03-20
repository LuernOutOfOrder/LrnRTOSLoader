COMPILER=riscv32-none-elf-gcc 
COMPILER_FLAGS=-march=rv32g -mabi=ilp32 -static -mcmodel=medany -fvisibility=hidden -nostdlib -nostartfiles -Tlinker.ld

SRC=main.S
OBJECTS=$(SOURCES:%.o: %.S)
BUILD_DIR=build/
OBJ_NAME=bootloader

LINKER=

run:
	qemu-system-riscv32

cmp:
	$(COMPILER) $(COMPILER_FLAGS) $(SRC) -o $(BUILD_DIR)$(OBJ_NAME)
