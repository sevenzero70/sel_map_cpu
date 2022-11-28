
all:
	@(cd sipgen; $(MAKE))
	@(cd siplib; $(MAKE))

install:
	@(cd sipgen; $(MAKE) install)
	@(cd siplib; $(MAKE) install)
	@test -d $(DESTDIR)/usr/lib/python3/dist-packages || mkdir -p $(DESTDIR)/usr/lib/python3/dist-packages
	cp -f sipconfig.py $(DESTDIR)/usr/lib/python3/dist-packages/sipconfig.py
	cp -f /home/xxx/sel_ws/src/sip-4.19.25/sipdistutils.py $(DESTDIR)/usr/lib/python3/dist-packages/sipdistutils.py
	/usr/bin/python /home/xxx/sel_ws/src/sip-4.19.25/mk_distinfo.py "$(DESTDIR)" /usr/lib/python3/dist-packages/sip-4.19.25.dist-info installed.txt

clean:
	@(cd sipgen; $(MAKE) clean)
	@(cd siplib; $(MAKE) clean)
