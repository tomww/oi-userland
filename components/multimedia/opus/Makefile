#
# This file and its contents are supplied under the terms of the
# Common Development and Distribution License ("CDDL"). You may
# only use this file in accordance with the terms of the CDDL.
#
# A full copy of the text of the CDDL should have accompanied this
# source. A copy of the CDDL is also available via the Internet at
# http://www.illumos.org/license/CDDL.
#

#
# Copyright 2013 EveryCity Ltd. All rights reserved.
# Copyright 2016 Aurelien Larcher. All rights reserved.
#

include ../../../make-rules/shared-macros.mk

COMPONENT_NAME=       opus
COMPONENT_VERSION=    1.1.3
COMPONENT_REVISION=   1
COMPONENT_PROJECT_URL=http://opus-codec.org/
COMPONENT_SUMMARY=    Opus is an open, royalty-free, versatile audio codec for interactive speech and music transmission over the Internet
COMPONENT_FMRI=       library/opus
COMPONENT_CLASSIFICATION= System/Libraries
COMPONENT_SRC=        $(COMPONENT_NAME)-$(COMPONENT_VERSION)
COMPONENT_ARCHIVE=    $(COMPONENT_SRC).tar.gz
COMPONENT_ARCHIVE_HASH=  \
    sha256:58b6fe802e7e30182e95d0cde890c0ace40b6f125cffc50635f0ad2eef69b633
COMPONENT_ARCHIVE_URL=http://downloads.xiph.org/releases/opus/$(COMPONENT_ARCHIVE)
COMPONENT_LICENSE=    BSD

include $(WS_MAKE_RULES)/prep.mk
include $(WS_MAKE_RULES)/configure.mk
include $(WS_MAKE_RULES)/ips.mk

PATH=/usr/gnu/bin:/usr/bin

ENV+= -i

CONFIGURE_OPTIONS+= --disable-static
CONFIGURE_OPTIONS+= --enable-shared

build:    $(BUILD_32_and_64)

install:  $(INSTALL_32_and_64)

test:  $(TEST_32_and_64)

REQUIRED_PACKAGES += system/library
REQUIRED_PACKAGES += system/library/math
