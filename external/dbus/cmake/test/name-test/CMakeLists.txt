if (DBUS_BUILD_TESTS)

set (NAMEtest-DIR ../../../test/name-test)

add_definitions(-DDBUS_COMPILATION)

add_executable(test-pending-call-dispatch ${NAMEtest-DIR}/test-pending-call-dispatch.c)
target_link_libraries(test-pending-call-dispatch ${DBUS_INTERNAL_LIBRARIES})
ADD_TEST(test-pending-call-dispatch ${EXECUTABLE_OUTPUT_PATH}/test-pending-call-dispatch)

add_executable(test-pending-call-timeout ${NAMEtest-DIR}/test-pending-call-timeout.c)
target_link_libraries(test-pending-call-timeout ${DBUS_INTERNAL_LIBRARIES})
ADD_TEST(test-pending-call-timeout ${EXECUTABLE_OUTPUT_PATH}/test-pending-call-timeout)

add_executable(test-thread-init ${NAMEtest-DIR}/test-threads-init.c)
target_link_libraries(test-thread-init ${DBUS_INTERNAL_LIBRARIES})
ADD_TEST(test-thread-init ${EXECUTABLE_OUTPUT_PATH}/test-thread-init)

add_executable(test-ids ${NAMEtest-DIR}/test-ids.c)
target_link_libraries(test-ids ${DBUS_INTERNAL_LIBRARIES})
ADD_TEST(test-ids ${EXECUTABLE_OUTPUT_PATH}/test-ids)

add_executable(test-shutdown ${NAMEtest-DIR}/test-shutdown.c)
target_link_libraries(test-shutdown ${DBUS_INTERNAL_LIBRARIES} dbus_testutils)
ADD_TEST(test-shutdown ${EXECUTABLE_OUTPUT_PATH}/test-shutdown)

add_executable(test-privserver ${NAMEtest-DIR}/test-privserver.c)
target_link_libraries(test-privserver ${DBUS_INTERNAL_LIBRARIES} dbus_testutils)
ADD_TEST(test-privserver ${EXECUTABLE_OUTPUT_PATH}/test-privserver)

add_executable(test-privserver-client ${NAMEtest-DIR}/test-privserver-client.c)
target_link_libraries(test-privserver-client ${DBUS_INTERNAL_LIBRARIES} dbus_testutils)
ADD_TEST(test-privserver-client ${EXECUTABLE_OUTPUT_PATH}/test-privserver-client)

endif (DBUS_BUILD_TESTS)
