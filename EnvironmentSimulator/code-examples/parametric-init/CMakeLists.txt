
include_directories (
  ${SCENARIOENGINE_DLL_INCLUDE_DIR}
  ${COMMON_MINI_INCLUDE_DIR}
)

set (TARGET parametric-init)

set ( SOURCES
  parametric-init.cpp
)

set ( INCLUDES
)

add_executable ( ${TARGET} ${SOURCES} ${INCLUDES} )

target_link_libraries (
	${TARGET}
	esminiLib
	CommonMini
    RoadManager
	${TIME_LIB}
)

install ( TARGETS ${TARGET} DESTINATION "${INSTALL_DIRECTORY_CODE_EXAMPLES}")
