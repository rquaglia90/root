# Copyright (C) 1995-2019, Rene Brun and Fons Rademakers.
# All rights reserved.
#
# For the licensing terms see $ROOTSYS/LICENSE.
# For the list of contributors see $ROOTSYS/README/CREDITS.

#######################################################################################
# CMakeLists.txt file for building JupyROOT bindings/pyroot_experimental/PyROOT package
#######################################################################################

set(JupyROOTDirName python/JupyROOT)

ROOT_LINKER_LIBRARY(JupyROOT src/IOHandler.cxx DEPENDENCIES Core CMAKENOEXPORT)

file(COPY ${JupyROOTDirName} DESTINATION ${localruntimedir})
install(DIRECTORY ${JupyROOTDirName} DESTINATION ${runtimedir})
