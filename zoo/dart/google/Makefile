extract:
	${slpsdir}/topics/extraction/antlr/antlrpp.py Dart.rsc.g Dart.prepared.g
	java -cp ${CLASSPATH}:${slpsdir}/download/antlrworks-1.1.7.jar:${slpsdir}/topics/extraction/antlr slps.antlr2bgf.Tool Dart.prepared.g raw.bgf
	${tooldir}/xbgf post-extraction.xbgf raw.bgf ext.bgf
	${tooldir}/subgrammar ext.bgf compilationUnit libraryUnit grammar.bgf

get:
	curl -k https://dart.googlecode.com/svn/branches/bleeding_edge/dart/language/grammar/Dart.g > fetched/Dart.g

include ../../Makefile.grammar
