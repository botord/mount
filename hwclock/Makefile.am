include $(top_srcdir)/config/include-Makefile.am

dist_man_MANS = hwclock.8

sbin_PROGRAMS = hwclock

hwclock_SOURCES = \
	clock.h \
	cmos.c \
	hwclock.c \
	kd.c \
	$(top_srcdir)/lib/strutils.c
hwclock_LDADD =

if LINUX
hwclock_SOURCES += rtc.c
endif

if HAVE_AUDIT
hwclock_LDADD += -laudit
endif
