AM_CPPFLAGS = \
	$(DBUS_CFLAGS) \
	$(GLIB_CFLAGS) \
	$(NM_CFLAGS) \
	-DG_DISABLE_DEPRECATED \
	-DBINDIR=\"$(bindir)\" \
	-DPREFIX=\""$(prefix)"\" \
	-DSYSCONFDIR=\""$(sysconfdir)"\" \
	-DVERSION="\"$(VERSION)\"" \
	-DLIBDIR=\""$(libdir)"\" \
	-DLIBEXECDIR=\""$(libexecdir)"\" \
	-DLOCALSTATEDIR=\""$(localstatedir)"\" \
	-DDATADIR=\"$(datadir)\" \
	-DNM_VPNC_LOCALEDIR=\"$(datadir)/locale\"

libexec_PROGRAMS = nm-vpnc-service nm-vpnc-service-vpnc-helper

nm_vpnc_service_SOURCES = \
	nm-vpnc-service.c \
	nm-vpnc-service.h \
	nm-vpnc-service-defines.h \
	utils.c \
	utils.h

nm_vpnc_service_LDADD = \
	$(DBUS_LIBS) \
	$(GLIB_LIBS) \
	$(NM_LIBS)


nm_vpnc_service_vpnc_helper_SOURCES = \
				nm-vpnc-service-vpnc-helper.c

nm_vpnc_service_vpnc_helper_LDADD = \
	$(DBUS_LIBS) \
	$(GTHREAD_LIBS) \
	$(NM_LIBS)

noinst_PROGRAMS = test-vpnc-output

test_vpnc_output_SOURCES = \
	test-vpnc-output.c \
	utils.c \
	utils.h

test_vpnc_output_LDADD = $(GLIB_LIBS)

check-local:
	$(abs_builddir)/test-vpnc-output

CLEANFILES = *~
