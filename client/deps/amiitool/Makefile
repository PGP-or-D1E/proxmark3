MYSRCPATHS =
MYINCLUDES = -I. -I.. -I../../../common -I../../../common/mbedtls -I../../../include -I../../src -I../../../include -I../jansson
MYCFLAGS =
MYDEFS =
MYSRCS = \
	amiibo.c \
	drbg.c \
	keygen.c

LIB_A = libamiibo.a

# Transition: remove old directories and objects
MYCLEANOLDPATH = ../../amiitool

include ../../../Makefile.host

# just for testing amiitool before complete migration into a lib:

amiitool:
	gcc $(CFLAGS) \
	  amiitool.c $(MYSRCS) ../../../common/commonutil.c ../ui.c -lreadline -lm ../../../common/mbedtls/libmbedtls.a \
	  -o amiitool
