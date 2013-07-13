cmake_minimum_required(VERSION 2.8.9)

if(NOT Slicer_SOURCE_DIR)

  #-----------------------------------------------------------------------------
  set(EXTENSION_NAME SimpleFilters)
  set(EXTENSION_HOMEPAGE "http://www.slicer.org/slicerWiki/index.php/Documentation/Nightly/Extensions/SimpleFilters")
  set(EXTENSION_CATEGORY "Filtering")
  set(EXTENSION_STATUS "Beta")
  set(EXTENSION_CONTRIBUTORS "Bradley Lowekamp (MSC/NLM)" )
  set(EXTENSION_DESCRIPTION "This is a meta module which contains interfaces for many Simple ITK image filters.")
  set(EXTENSION_ICONURL "http://viewvc.slicer.org/viewvc.cgi/Slicer4/trunk/Extensions/Testing/SimpleFilters/SimpleFilters.png?revision=21747&view=co")
  set(EXTENSION_SCREENSHOTURLS "http://wiki.slicer.org/slicerWiki/images/e/e2/Slicer-r19441-SimpleFilters-screenshot.png")

  set(EXTENSION_LICENSE_FILE ${Slicer_LICENSE_FILE})
  set(EXTENSION_README_FILE ${Slicer_README_FILE})


  #-----------------------------------------------------------------------------
  find_package(Slicer REQUIRED)
  include(${Slicer_USE_FILE})


endif()


#-----------------------------------------------------------------------------
# Module Subdirectories
#-----------------------------------------------------------------------------
add_subdirectory(SimpleFilters)

#-----------------------------------------------------------------------------
# Packaging
#-----------------------------------------------------------------------------
if(NOT Slicer_SOURCE_DIR)
  include(${Slicer_EXTENSION_CPACK})
endif()
