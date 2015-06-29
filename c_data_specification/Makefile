# An example Makefile suitable for use in SpiNNaker applications using the
# spinnaker_tools libraries and makefiles.

# The name of the application to be built (binary will be this with a `.aplx`
# extension)
APP = data_specification_executor

LIBRARIES = $(SPINN_DIRS)/lib/libspinn_frontend_common.a -lspinn_common $(SPINN_DIRS)/lib/libspin1_api.a -lm

# Directory to create APLX files in (must include trailing slash)
APP_OUTPUT_DIR = ./

# Directory to place compilation artefacts (must include trailing slash)
BUILD_DIR = ./

# A space-separated list of object files to be built into the executable. These
# .o files will be created from corresponding .c files (e.g. example.c in this
# case).
OBJECTS = data_specification_executor_functions.o data_specification_executor.o 

# The spinnaker_tools standard makefile
include $(SPINN_DIRS)/Makefile.common

all: $(APP_OUTPUT_DIR)$(APP).aplx

clean:
	$(RM) $(OBJECTS) $(BUILD_DIR)$(APP).elf $(BUILD_DIR)$(APP).txt $(APP_OUTPUT_DIR)$(APP).aplx
