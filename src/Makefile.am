bin_PROGRAMS = tlc

EXTRA_DIST = ast stdlib libthorn
INCLUDES = -I$(top_srcdir)/jsoncpp/include
AM_CXXFLAGS = -I`$(top_srcdir)/llvm-config --includedir --cxxflags` -fexceptions -frtti -Wall -Wextra -Wno-unused-parameter \
	      -Wno-overloaded-virtual
LIBS = `$(top_srcdir)/llvm-config --cxxflags --ldflags \
	    --libs --system-libs` \
	-ljson

AM_LDFLAGS = -L/opt/local/lib

tlc_SOURCES = main.cpp modgen.cpp json_parser.cpp ast/expression.cpp			\
			  ast/parser.cpp lexscope.cpp lexentry.cpp ast/undefdvars.cpp		\
			  ast/unit.cpp ast/vardef.cpp ast/literal.cpp ast/closure.cpp   \
			  ast/var.cpp ast/block.cpp	ast/methodcall.cpp ast/object.cpp	\
			  ast/if.cpp ast/return.cpp	ast/assignment.cpp ast/while.cpp		\
			  ast/array.cpp	str_util.cpp ast/count_assignments.cpp				\
			  ast/try.cpp ast/throw.cpp ast/spawn.cpp ast/send.cpp builder.cpp	\
			  ast/const_precalc.cpp ast/visitor.cpp ast/tree_printer.cpp

#tlc_LDADD = -lboost_program_options-mt
