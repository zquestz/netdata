#
# Copyright (C) 2015 Alon Bar-Lev <alon.barlev@gmail.com>
#
MAINTAINERCLEANFILES= $(srcdir)/Makefile.in

dist_web_DATA = \
        robots.txt \
        index.html \
	demo.html \
	demo2.html \
	tv.html \
        dashboard.html \
        dashboard.js \
        dashboard.css \
        dashboard.slate.css \
	favicon.ico \
	netdata-swagger.yaml \
	netdata-swagger.json \
        version.txt \
        $(NULL)

webolddir=$(webdir)/old
dist_webold_DATA = \
        old/datasource.html \
        old/index.html \
        old/index.js \
        old/netdata.js \
        old/theme.css \
        $(NULL)

weblibdir=$(webdir)/lib
dist_weblib_DATA = \
        lib/dygraph-combined.js \
        lib/dygraph-smooth-plotter.js \
        lib/jquery-1.12.0.min.js \
        lib/jquery.peity.min.js \
        lib/jquery.sparkline.min.js \
        lib/morris.min.js \
        lib/raphael-min.js \
	lib/jquery.easypiechart.min.js \
	lib/jquery.nanoscroller.min.js \
        lib/bootstrap.min.js \
	lib/ElementQueries.js \
	lib/ResizeSensor.js \
        lib/bootstrap-toggle.min.js \
        lib/c3.min.js \
        lib/d3.min.js \
        lib/gauge.min.js \
        $(NULL)

webcssdir=$(webdir)/css
dist_webcss_DATA = \
        css/morris.css \
        css/bootstrap.min.css \
        css/bootstrap-theme.min.css \
        css/bootstrap.slate.min.css \
	css/font-awesome.min.css \
        css/bootstrap-toggle.min.css \
        css/c3.min.css \
        $(NULL)

webfontsdir=$(webdir)/fonts
dist_webfonts_DATA = \
        fonts/glyphicons-halflings-regular.eot \
        fonts/glyphicons-halflings-regular.svg \
        fonts/glyphicons-halflings-regular.ttf \
        fonts/glyphicons-halflings-regular.woff \
        fonts/glyphicons-halflings-regular.woff2 \
	fonts/FontAwesome.otf \
	fonts/fontawesome-webfont.eot \
	fonts/fontawesome-webfont.svg \
	fonts/fontawesome-webfont.ttf \
	fonts/fontawesome-webfont.woff \
	fonts/fontawesome-webfont.woff2 \
        $(NULL)

webimagesdir=$(webdir)/images
dist_webimages_DATA = \
	images/seo-performance-16.png \
	images/seo-performance-24.png \
	images/seo-performance-32.png \
	images/seo-performance-48.png \
	images/seo-performance-64.png \
	images/seo-performance-72.png \
	images/seo-performance-114.png \
	images/seo-performance-128.png \
	images/seo-performance-256.png \
	images/seo-performance-512.png \
	images/seo-performance-multi-size.ico \
	images/seo-performance-multi-size.icns \
        $(NULL)

version.txt:
	if test -d "$(top_srcdir)/.git"; then \
		if git --git-dir="$(top_srcdir)/.git" log -n 1 > v.tmp; then \
			grep ^commit\  v.tmp | cut -d" " -f2 > version.txt; \
			rm -f v.tmp; \
		else \
			rm -f v.tmp; \
			echo "0" > version.txt; \
		fi; \
	else \
		echo "0" > version.txt; \
	fi

.PHONY: version.txt
