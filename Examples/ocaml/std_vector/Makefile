TOP        = ../..
SWIGEXE    = $(TOP)/../swig
SWIG_LIB_DIR = $(TOP)/../$(TOP_BUILDDIR_TO_TOP_SRCDIR)Lib
SRCS       =
TARGET     = example
INTERFACE  = example.i
PROGFILE   = runme.ml

check: build
	$(MAKE) -f $(TOP)/Makefile SRCDIR='$(SRCDIR)' TARGET='$(TARGET)' ocaml_run

build: static

static:
	$(MAKE) -f $(TOP)/Makefile SRCDIR='$(SRCDIR)' SRCS='$(SRCS)' \
	SWIG_LIB_DIR='$(SWIG_LIB_DIR)' SWIGEXE='$(SWIGEXE)' \
	PROGFILE='$(PROGFILE)' TARGET='$(TARGET)' INTERFACE='$(INTERFACE)' \
	ocaml_core
	$(MAKE) -f $(TOP)/Makefile SRCDIR='$(SRCDIR)' SRCS='$(SRCS)' \
	SWIG_LIB_DIR='$(SWIG_LIB_DIR)' SWIGEXE='$(SWIGEXE)' \
	PROGFILE='$(PROGFILE)' TARGET='$(TARGET)' INTERFACE='$(INTERFACE)' \
	ocaml_static_cpp

dynamic:
	$(MAKE) -f $(TOP)/Makefile SRCDIR='$(SRCDIR)' SRCS='$(SRCS)' \
	SWIG_LIB_DIR='$(SWIG_LIB_DIR)' SWIGEXE='$(SWIGEXE)' \
	PROGFILE='$(PROGFILE)' TARGET='$(TARGET)' INTERFACE='$(INTERFACE)' \
	ocaml_dynamic_cpp

clean:
	$(MAKE) -f $(TOP)/Makefile SRCDIR='$(SRCDIR)' TARGET='$(TARGET)' ocaml_clean
