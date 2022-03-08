VERSION=5.18.2-bone6

MRF89XA-CAPE-00A2.dtbo: MRF89XA-CAPE-00A2.dts
	gcc -E -Wp,-MD,MRF89XA-CAPE-00A2.pre.tmp -nostdinc -I/lib/modules/${VERSION}/build/include -undef -D__DTS__ -x assembler-with-cpp MRF89XA-CAPE-00A2.dts > MRF89XA-CAPE-00A2.processed.dts
	dtc -@ -o MRF89XA-CAPE-00A2.dtbo MRF89XA-CAPE-00A2.processed.dts
	rm -f MRF89XA-CAPE-00A2.processed.dts MRF89XA-CAPE-00A2.pre.tmp

install: MRF89XA-CAPE-00A2.dtbo
	cp MRF89XA-CAPE-00A2.dtbo /lib/firmware/MRF89XA-CAPE-00A2.dtbo

.PHONY: install
