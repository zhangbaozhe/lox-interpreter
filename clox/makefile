SOURCE_DIR := src
BUILD_DIR := build
HEADERS := $(wildcard $(SOURCE_DIR)/*.h)
SOURCES := $(wildcard $(SOURCE_DIR)/*.c)
OBJECTS := $(addprefix $(BUILD_DIR)/, $(notdir $(SOURCES:.c=.o)))

clox: $(OBJECTS)
	gcc $^ -o $(BUILD_DIR)/$@

$(BUILD_DIR)/%.o: $(SOURCE_DIR)/%.c $(HEADERS)
	gcc -c -o $@ $<

.PHONY:
clean:
	rm -rf $(BUILD_DIR)/*