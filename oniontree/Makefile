OUTPUT=../public/oniontree
TARGETS=all.json

.PHONY: all
all: $(addprefix $(OUTPUT)/,$(TARGETS))

.PHONY: clean
clean:
	$(RM) $(addprefix $(OUTPUT)/,$(TARGETS))

$(addprefix $(OUTPUT)/,$(TARGETS)):
	oniontree-generate \
		-oniontree "$(ONIONTREE_PATH)" \
		-with-description=false \
		-with-public-keys=false \
		-template "$(notdir $@).in" > "$@"

