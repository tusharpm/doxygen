# vim:ts=4:sw=4:expandtab:autoindent:

add_library(vhdlparser STATIC
    CharStream.cc
    ParseException.cc
    Token.cc
    TokenMgrError.cc
    VhdlParser.cc
    VhdlParserTokenManager.cc
    VhdlParserIF.cpp
)
add_dependencies(vhdlparser doxycfg)
target_include_directories(vhdlparser PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}
    ${TOP}/src
    ${TOP}/qtools
    ${GENERATED_SRC}
)
