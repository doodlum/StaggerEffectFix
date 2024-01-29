cmake_minimum_required(VERSION 3.20)

project(
	StaggerEffectFix
	VERSION 1.0.1
	LANGUAGES CXX
)

list(APPEND CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/cmake")
include(XSEPlugin)

add_subdirectory("extern/DKUtil" DKUtil)

target_link_libraries(
	"${PROJECT_NAME}"
	PRIVATE
		DKUtil::DKUtil
)