THISDIR := potentialMethods
THISBOOK := $(THISDIR)
BASEVER := 8aa2fcd

include ../latex/make.vars

FIGURES := ../figures
SOURCE_DIRS += $(FIGURES)

GENERATED_PDFS += $(THISBOOK).pdf

EPS_FILES := $(wildcard $(FIGURES)/*.eps)
PDFS_FROM_EPS := $(subst eps,pdf,$(EPS_FILES))

THISBOOK_DEPS += $(PDFS_FROM_EPS)
CLEAN_TARGETS += Bibliography.bib

all :: myrefs.bib $(GENERATED_PDFS)

$(GENERATED_PDFS) :: $(JUSTBOOKDEPENDENCIES) $(LOCAL_FILES) $(GENERATED_SOURCES) $(COPIED_FILES) $(LOCAL_COPIED_FILES)
$(THISBOOK).pdf :: $(PDFS_FROM_EPS)
$(THISBOOK).pdf :: Bibliography.bib

include ../latex/make.rules
