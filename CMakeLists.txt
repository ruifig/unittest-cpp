cmake_minimum_required(VERSION 3.5)

set (SOURCE_FILES
	"UnitTest++/AssertException.cpp"
	"UnitTest++/AssertException.h"
	"UnitTest++/CheckMacros.h"
	"UnitTest++/Checks.cpp"
	"UnitTest++/Checks.h"
	"UnitTest++/CompositeTestReporter.cpp"
	"UnitTest++/CompositeTestReporter.h"
	"UnitTest++/Config.h"
	"UnitTest++/CurrentTest.cpp"
	"UnitTest++/CurrentTest.h"
	"UnitTest++/DeferredTestReporter.cpp"
	"UnitTest++/DeferredTestReporter.h"
	"UnitTest++/DeferredTestResult.cpp"
	"UnitTest++/DeferredTestResult.h"
	"UnitTest++/ExceptionMacros.h"
	"UnitTest++/ExecuteTest.h"
	"UnitTest++/HelperMacros.h"
	"UnitTest++/Makefile.am"
	"UnitTest++/MemoryOutStream.cpp"
	"UnitTest++/MemoryOutStream.h"
	"UnitTest++/ReportAssert.cpp"
	"UnitTest++/ReportAssert.h"
	"UnitTest++/ReportAssertImpl.h"
	"UnitTest++/RequiredCheckException.cpp"
	"UnitTest++/RequiredCheckException.h"
	"UnitTest++/RequiredCheckTestReporter.cpp"
	"UnitTest++/RequiredCheckTestReporter.h"
	"UnitTest++/RequireMacros.h"
	"UnitTest++/Test.cpp"
	"UnitTest++/Test.h"
	"UnitTest++/TestDetails.cpp"
	"UnitTest++/TestDetails.h"
	"UnitTest++/TestList.cpp"
	"UnitTest++/TestList.h"
	"UnitTest++/TestMacros.h"
	"UnitTest++/TestReporter.cpp"
	"UnitTest++/TestReporter.h"
	"UnitTest++/TestReporterStdout.cpp"
	"UnitTest++/TestReporterStdout.h"
	"UnitTest++/TestResults.cpp"
	"UnitTest++/TestResults.h"
	"UnitTest++/TestRunner.cpp"
	"UnitTest++/TestRunner.h"
	"UnitTest++/TestSuite.h"
	"UnitTest++/ThrowingTestReporter.cpp"
	"UnitTest++/ThrowingTestReporter.h"
	"UnitTest++/TimeConstraint.cpp"
	"UnitTest++/TimeConstraint.h"
	"UnitTest++/TimeHelpers.h"
	"UnitTest++/UnitTest++.h"
	"UnitTest++/UnitTestPP.h"
	"UnitTest++/XmlTestReporter.cpp"
	"UnitTest++/XmlTestReporter.h"
	)

if (WIN32)
	list(APPEND SOURCE_FILES
		"UnitTest++/Win32/TimeHelpers.cpp"
		"UnitTest++/Win32/TimeHelpers.h"
	)
else()
	list(APPEND SOURCE_FILES
		"UnitTest++/Posix/SignalTranslator.cpp"
		"UnitTest++/Posix/SignalTranslator.h"
		"UnitTest++/Posix/TimeHelpers.cpp"
		"UnitTest++/Posix/TimeHelpers.h"
	)
endif()

add_library(UnitTest++ STATIC ${SOURCE_FILES})
target_include_directories(UnitTest++ PUBLIC "")

