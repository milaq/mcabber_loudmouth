include $(top_srcdir)/build/Makefile.am.lm

SUBDIRS = loudmouth docs examples $(TEST_DIRS)
DIST_SUBDIRS = loudmouth docs examples tests

EXTRA_DIST +=			\
	loudmouth-1.0.pc.in     \
	README.WIN32

pkgconfigdir = $(libdir)/pkgconfig
pkgconfig_DATA = loudmouth-1.0.pc

DISTCHECK_CONFIGURE_FLAGS =     \
	--enable-gtk-doc

ChangeLog: OLD_VERSION=`git describe`
ChangeLog:
	git log --no-merges $(OLD_VERSION)..HEAD > $(srcdir)/ChangeLog
