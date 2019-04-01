COPT=-DMEGA65 -I. -I../uip -I../apps/resolv -I../apps/webclient 
# -I../apps/dhcpc

uip.prg:
#	cc65 $(COPT) ../apps/resolv/resolv.c
	cc65 $(COPT) ../apps/webclient/webclient.c
	cc65 $(COPT) ../apps/webclient/webclient-strings.c
	cc65 $(COPT) main.c 
	cc65 $(COPT) mega65ethdev.c 
	cc65 $(COPT) clock-arch.c
	cc65 $(COPT) ../uip/psock.c
	cc65 $(COPT) ../uip/timer.c
	cc65 $(COPT) ../uip/uip_arp.c
	cc65 $(COPT) ../uip/uip.c
	cc65 $(COPT) ../uip/uip-fw.c
	cc65 $(COPT) ../uip/uiplib.c
	cc65 $(COPT) ../uip/uip-neighbor.c
	cl65 -vm -m mega65.map -o uip.prg *.s ../uip/*.s ../apps/*/*.s

clean:
	rm *.s ../uip/*.s ../apps/*/*.s uip.prg
