add_executable(quicksort quicksort.cpp )
include_directories(../include)
set_target_properties(quicksort PROPERTIES CXX_STANDARD 17)
IF(${CMAKE_SYSTEM_NAME} MATCHES "Linux")
	target_link_libraries(quicksort PUBLIC pthread)
ENDIF()
#function(config n m h)
#  add_executable("test${n}" test-main.cpp "t${n}.cpp" "${h}")
  #pass the option -DPARTIAL if you want partial grades
 # set(MYOPT "-DMAX_POINTS=${m};-DTEST_NAME=\"Test${n}\"")
  #  message(${MYOPT})
  #this will set preprocessor flags for ALL of them
  #add_compile_definitions(MAX_POINTS=${m} TEST_NAME="Test${n}")
 # set_source_files_properties("t${n}.cpp" PROPERTIES COMPILE_OPTIONS "-DMAX_POINTS=${m};-DTEST_NAME=\"Test${n}\"")
  #set_source_files_properties("t${n}.cpp" PROPERTIES COMPILE_OPTIONS ${MYOPT})
 # set_target_properties(test${n} PROPERTIES CXX_STANDARD 17)
#endfunction()

#config(0 10 "../include/max_sub_sum.h")
#config(1 10 "../include/max_sub_sum.h")
#config(2 10  "../include/peak.h")
#config(3 10  "../include/stock.h")
#get_cmake_property(_variableNames VARIABLES)
#list (SORT _variableNames)
#foreach (_variableName ${_variableNames})
#	    message(STATUS "${_variableName}=${${_variableName}}")
#    endforeach()

