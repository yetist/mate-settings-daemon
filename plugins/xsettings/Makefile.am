NULL =

plugin_LTLIBRARIES = \
	libxsettings.la		\
	$(NULL)

libxsettings_la_SOURCES = 	\
	msd-xsettings-plugin.h	\
	msd-xsettings-plugin.c	\
	msd-xsettings-manager.h	\
	msd-xsettings-manager.c	\
	xsettings-common.h	\
	xsettings-common.c	\
	xsettings-manager.h	\
	xsettings-manager.c	\
	fontconfig-monitor.h	\
	fontconfig-monitor.c	\
	wm-common.h	\
	wm-common.c	\
	$(NULL)

libxsettings_la_CPPFLAGS = \
	-I$(top_srcdir)/mate-settings-daemon		\
	-DMATE_SETTINGS_LOCALEDIR=\""$(datadir)/locale"\" \
	$(AM_CPPFLAGS)

libxsettings_la_CFLAGS = \
	$(SETTINGS_PLUGIN_CFLAGS)	\
	$(FONTCONFIG_CFLAGS)		\
	$(AM_CFLAGS)

libxsettings_la_LDFLAGS = 	\
	$(MSD_PLUGIN_LDFLAGS)	\
	$(NULL)

libxsettings_la_LIBADD  = 	\
	$(SETTINGS_PLUGIN_LIBS)	\
	$(FONTCONFIG_LIBS)	\
	$(NULL)

plugin_in_files = 		\
	xsettings.mate-settings-plugin.in	\
	$(NULL)

plugin_DATA = $(plugin_in_files:.mate-settings-plugin.in=.mate-settings-plugin)

EXTRA_DIST = 			\
	$(plugin_in_files)	\
	$(NULL)

CLEANFILES = 			\
	$(plugin_DATA)		\
	$(NULL)

DISTCLEANFILES =		\
	$(plugin_DATA)		\
	$(NULL)

@MSD_INTLTOOL_PLUGIN_RULE@
