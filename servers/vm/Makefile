# Makefile for VM server
.include <bsd.own.mk>

PROG=	vm
SRCS=	main.c alloc.c utility.c exec.c exit.c fork.c break.c \
	signal.c mmap.c slaballoc.c region.c pagefaults.c addravl.c \
	physravl.c rs.c queryexit.c yieldedavl.c regionavl.c

DPADD+=	${LIBSYS}
LDADD+=	-lsys

MAN=

BINDIR?= /usr/sbin

CPPFLAGS+= -I${.CURDIR} -I${.CURDIR}/arch/${MACHINE_ARCH}
CPPFLAGS+=	-I${NETBSDSRCDIR}

.include "arch/${MACHINE_ARCH}/Makefile.inc"
.include <minix.bootprog.mk>
