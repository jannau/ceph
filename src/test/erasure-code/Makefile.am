check_SCRIPTS += \
	test/erasure-code/test-erasure-code.sh

ceph_erasure_code_benchmark_SOURCES = \
	test/erasure-code/ceph_erasure_code_benchmark.cc
ceph_erasure_code_benchmark_LDADD = $(LIBOSD) $(LIBCOMMON) $(BOOST_PROGRAM_OPTIONS_LIBS) $(CEPH_GLOBAL)
if LINUX
ceph_erasure_code_benchmark_LDADD += -ldl
endif
bin_DEBUGPROGRAMS += ceph_erasure_code_benchmark

ceph_erasure_code_SOURCES = \
	test/erasure-code/ceph_erasure_code.cc
ceph_erasure_code_LDADD = $(LIBOSD) $(LIBCOMMON) $(BOOST_PROGRAM_OPTIONS_LIBS) $(CEPH_GLOBAL)
if LINUX
ceph_erasure_code_LDADD += -ldl
endif
bin_DEBUGPROGRAMS += ceph_erasure_code

libec_example_la_SOURCES = test/erasure-code/ErasureCodePluginExample.cc
test/erasure-code/ErasureCodePluginExample.cc: ./ceph_ver.h
libec_example_la_CFLAGS = ${AM_CFLAGS}
libec_example_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_example_la_LIBADD = $(LIBCRUSH) $(PTHREAD_LIBS) $(EXTRALIBS)
libec_example_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_example.la

libec_missing_entry_point_la_SOURCES = test/erasure-code/ErasureCodePluginMissingEntryPoint.cc
test/erasure-code/ErasureCodePluginMissingEntryPoint.cc: ./ceph_ver.h
libec_missing_entry_point_la_CFLAGS = ${AM_CFLAGS}
libec_missing_entry_point_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_missing_entry_point_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_missing_entry_point_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_missing_entry_point.la

libec_missing_version_la_SOURCES = test/erasure-code/ErasureCodePluginMissingVersion.cc
libec_missing_version_la_CFLAGS = ${AM_CFLAGS}
libec_missing_version_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_missing_version_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_missing_version_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_missing_version.la

libec_hangs_la_SOURCES = test/erasure-code/ErasureCodePluginHangs.cc
test/erasure-code/ErasureCodePluginHangs.cc: ./ceph_ver.h
libec_hangs_la_CFLAGS = ${AM_CFLAGS}
libec_hangs_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_hangs_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_hangs_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_hangs.la

libec_fail_to_initialize_la_SOURCES = test/erasure-code/ErasureCodePluginFailToInitialize.cc
test/erasure-code/ErasureCodePluginFailToInitialize.cc: ./ceph_ver.h
libec_fail_to_initialize_la_CFLAGS = ${AM_CFLAGS}
libec_fail_to_initialize_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_fail_to_initialize_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_fail_to_initialize_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_fail_to_initialize.la

libec_fail_to_register_la_SOURCES = test/erasure-code/ErasureCodePluginFailToRegister.cc
test/erasure-code/ErasureCodePluginFailToRegister.cc: ./ceph_ver.h
libec_fail_to_register_la_CFLAGS = ${AM_CFLAGS}
libec_fail_to_register_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_fail_to_register_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_fail_to_register_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_fail_to_register.la

libec_test_jerasure_sse4_la_SOURCES = test/erasure-code/TestJerasurePluginSSE4.cc
test/erasure-code/TestJerasurePluginSSE4.cc: ./ceph_ver.h
libec_test_jerasure_sse4_la_CFLAGS = ${AM_CFLAGS}
libec_test_jerasure_sse4_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_test_jerasure_sse4_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_test_jerasure_sse4_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_test_jerasure_sse4.la

libec_test_jerasure_sse3_la_SOURCES = test/erasure-code/TestJerasurePluginSSE3.cc
test/erasure-code/TestJerasurePluginSSE3.cc: ./ceph_ver.h
libec_test_jerasure_sse3_la_CFLAGS = ${AM_CFLAGS}
libec_test_jerasure_sse3_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_test_jerasure_sse3_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_test_jerasure_sse3_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_test_jerasure_sse3.la

libec_test_jerasure_generic_la_SOURCES = test/erasure-code/TestJerasurePluginGeneric.cc
test/erasure-code/TestJerasurePluginGeneric.cc: ./ceph_ver.h
libec_test_jerasure_generic_la_CFLAGS = ${AM_CFLAGS}
libec_test_jerasure_generic_la_CXXFLAGS= ${AM_CXXFLAGS}
libec_test_jerasure_generic_la_LIBADD = $(PTHREAD_LIBS) $(EXTRALIBS)
libec_test_jerasure_generic_la_LDFLAGS = ${AM_LDFLAGS} -export-symbols-regex '.*__erasure_code_.*'
erasure_codelib_LTLIBRARIES += libec_test_jerasure_generic.la

unittest_erasure_code_plugin_SOURCES = \
	erasure-code/ErasureCode.cc \
	test/erasure-code/TestErasureCodePlugin.cc 
unittest_erasure_code_plugin_CXXFLAGS = $(UNITTEST_CXXFLAGS)
unittest_erasure_code_plugin_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL)
if LINUX
unittest_erasure_code_plugin_LDADD += -ldl
endif
check_PROGRAMS += unittest_erasure_code_plugin

unittest_erasure_code_jerasure_SOURCES = \
	test/erasure-code/TestErasureCodeJerasure.cc \
	${jerasure_sources}
unittest_erasure_code_jerasure_CFLAGS = $(AM_CFLAGS) \
	-Ierasure-code/jerasure/gf-complete/include \
	-Ierasure-code/jerasure/jerasure/include
unittest_erasure_code_jerasure_CXXFLAGS = $(UNITTEST_CXXFLAGS) \
	-Ierasure-code/jerasure/gf-complete/include \
	-Ierasure-code/jerasure/jerasure/include
unittest_erasure_code_jerasure_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL)
if LINUX
unittest_erasure_code_jerasure_LDADD += -ldl
endif
check_PROGRAMS += unittest_erasure_code_jerasure

unittest_erasure_code_plugin_jerasure_SOURCES = \
	test/erasure-code/TestErasureCodePluginJerasure.cc
unittest_erasure_code_plugin_jerasure_CXXFLAGS = ${AM_CXXFLAGS} ${UNITTEST_CXXFLAGS}
unittest_erasure_code_plugin_jerasure_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL)
if LINUX
unittest_erasure_code_plugin_jerasure_LDADD += -ldl
endif
check_PROGRAMS += unittest_erasure_code_plugin_jerasure

if WITH_BETTER_YASM_ELF64
unittest_erasure_code_isa_SOURCES = \
	erasure-code/ErasureCode.cc \
	test/erasure-code/TestErasureCodeIsa.cc
unittest_erasure_code_isa_CXXFLAGS = ${AM_CXXFLAGS} ${UNITTEST_CXXFLAGS}
unittest_erasure_code_isa_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL) .libs/libec_isa.la $(LIBERASURE_CODE)
if LINUX
unittest_erasure_code_isa_LDADD += -ldl
endif
check_PROGRAMS += unittest_erasure_code_isa

unittest_erasure_code_plugin_isa_SOURCES = \
	erasure-code/ErasureCode.cc \
	test/erasure-code/TestErasureCodePluginIsa.cc
unittest_erasure_code_plugin_isa_CXXFLAGS = ${AM_CXXFLAGS} ${UNITTEST_CXXFLAGS}
unittest_erasure_code_plugin_isa_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL) .libs/libec_isa.la $(LIBERASURE_CODE)
if LINUX
unittest_erasure_code_plugin_isa_LDADD += -ldl
endif
check_PROGRAMS += unittest_erasure_code_plugin_isa
endif

unittest_erasure_code_lrc_SOURCES = \
	test/erasure-code/TestErasureCodeLrc.cc \
	${lrc_sources}
unittest_erasure_code_lrc_CXXFLAGS = $(UNITTEST_CXXFLAGS)
unittest_erasure_code_lrc_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL)
if LINUX
unittest_erasure_code_lrc_LDADD += -ldl
endif
check_PROGRAMS += unittest_erasure_code_lrc

unittest_erasure_code_plugin_lrc_SOURCES = \
	test/erasure-code/TestErasureCodePluginLrc.cc
unittest_erasure_code_plugin_lrc_CXXFLAGS = ${AM_CXXFLAGS} ${UNITTEST_CXXFLAGS}
unittest_erasure_code_plugin_lrc_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL)
if LINUX
unittest_erasure_code_plugin_lrc_LDADD += -ldl
endif
check_PROGRAMS += unittest_erasure_code_plugin_lrc

unittest_erasure_code_example_SOURCES = \
	erasure-code/ErasureCode.cc \
	test/erasure-code/TestErasureCodeExample.cc
noinst_HEADERS += test/erasure-code/ErasureCodeExample.h
unittest_erasure_code_example_CXXFLAGS = $(UNITTEST_CXXFLAGS)
unittest_erasure_code_example_LDADD = $(LIBOSD) $(LIBCOMMON) $(UNITTEST_LDADD) $(CEPH_GLOBAL)
check_PROGRAMS += unittest_erasure_code_example

noinst_HEADERS += \
	test/erasure-code/ceph_erasure_code_benchmark.h
