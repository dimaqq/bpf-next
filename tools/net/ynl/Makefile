# SPDX-License-Identifier: GPL-2.0

SUBDIRS = lib generated samples

all: $(SUBDIRS)
	./ynl-regen.sh -f -p $(PWD)/../../../

$(SUBDIRS):
	@if [ -f "$@/Makefile" ] ; then \
		$(MAKE) -C $@ ; \
	fi

clean hardclean:
	@for dir in $(SUBDIRS) ; do \
		if [ -f "$$dir/Makefile" ] ; then \
			$(MAKE) -C $$dir $@; \
		fi \
	done

.PHONY: clean all $(SUBDIRS)
