project(test_contract)

set(EOSIO_WASM_OLD_BEHAVIOR "Off")
find_package(eosio.cdt)

add_contract( test_contract test_contract test_contract.cpp )
target_include_directories( test_contract PUBLIC ${CMAKE_SOURCE_DIR}/../include )
target_ricardian_directory( test_contract ${CMAKE_SOURCE_DIR}/../ricardian )