
CPP=g++

CPPFLAGS=-O9 -DNDEBUG -Wall -I../includes/
#CPPFLAGS=-g3 -Wall -O0 -I../includes/  -pg
#CPPFLAGS=-O3 -Wall -DNDEBUG -I../includes/ -g3 -pg
INCS=-I../includes/
LIB=../lib/libcds.a

OBJECTS= testArray.o testBitSequence.o testSequence.o testHuffman.o testTextIndex.o testLCP.o testNPR.o testSuffixTree.o timeSequence.o toArray.o toArray2.o  intersection.o
BIN= testArray testBitSequence testSequence testHuffman testTextIndex testLCP testNPR testSuffixTree timeSequence toArray toArray2 intersection

%.o: %.cpp
	@echo " [C++] Compiling $<"
	@$(CPP) $(CPPFLAGS) $(INCS) -c $< -o $@

all: clean $(OBJECTS) $(BIN)
	@echo " [MSG] Done compiling tests"
	@echo " [FLG] $(CPPFLAGS)"

intersection:
	@echo " [LNK] Building intersection"
	@$(CPP) $(CPPFLAGS) -o intersection intersection.o $(LIB)

testHuffman:
	@echo " [LNK] Building testHuffman"
	@$(CPP) $(CPPFLAGS) -o testHuffman testHuffman.o $(LIB)

testSequence:
	@echo " [LNK] Building testSequence"
	@$(CPP) $(CPPFLAGS) -o testSequence testSequence.o $(LIB)

testBitSequence:
	@echo " [LNK] Building testBitSequence"
	@$(CPP) $(CPPFLAGS) -o testBitSequence testBitSequence.o $(LIB)

testArray:
	@echo " [LNK] Building testArray"
	@$(CPP) $(CPPFLAGS) -o testArray testArray.o $(LIB)

testTextIndex:
	 @echo " [LNK] Building testTextIndex"
	 @$(CPP) $(CPPFLAGS) -o testTextIndex testTextIndex.o $(LIB)

testLCP:
	@echo " [LNK] Building testLCP"
	@$(CPP) $(CPPFLAGS) -o testLCP testLCP.o $(LIB)

testNPR:
	@echo " [LNK] Building testNPR"
	@$(CPP) $(CPPFLAGS) -o testNPR testNPR.o $(LIB)

toArray2:
	@echo " [LNK] Building toArray2"
	@$(CPP) $(CPPFLAGS) -o toArray2 toArray2.o $(LIB)


toArray:
	@echo " [LNK] Building toArray"
	@$(CPP) $(CPPFLAGS) -o toArray toArray.o $(LIB)

testSuffixTree:
	@echo " [LNK] Building testSuffixTree"
	@$(CPP) $(CPPFLAGS) -o testSuffixTree testSuffixTree.o $(LIB)

timeSequence:
	@echo " [LNK] Building timeSequence"
	@$(CPP) $(CPPFLAGS) -o timeSequence timeSequence.o $(LIB)



clean:
	@echo " [CLN] Cleaning object and binary files"
	@rm -f $(OBJECTS) $(BIN)
