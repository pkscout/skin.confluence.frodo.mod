TARGET=Textures.xbt
XBMCTEX=/Users/Shared/buildslave/osx-64-nightly/build/tools/TexturePacker/TexturePacker

IMAGES := $(shell find . -name "*jpg")
IMAGES += $(shell find . -name "*png")
IMAGES += $(shell find . -name "*gif")

all: $(TARGET)

.PHONY: force

$(TARGET): $(XBMCTEX) $(IMAGES)
ifeq (,1)
	$(XBMCTEX) -use_none -input . -output $(TARGET)
else
	$(XBMCTEX) -input . -output $(TARGET)

endif
$(XBMCTEX): force
	$(MAKE) -C /Users/Shared/buildslave/osx-64-nightly/build/tools/TexturePacker

clean:
	rm -f $(TARGET)
distclean: clean

