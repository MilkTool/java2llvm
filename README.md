
# java2llvm

An Example Project Show Convert Java Byte Code to LLVM IR assembler , compile standalone executable file

This project is based on [class2ir](https://github.com/MParygin/class2ir), it based on an old llvm version.
So i changed some instruct syntex, and repaired bug, enhanced functionly.

Currently:
Tested CentOS x64 executable file, and say "Hello world".

Make:
1. Enter directory java2llvm/
2. Run build.sh, then you will get app.exe here.

Request:
java
llvm / clang
make

Known issue:
1. No GC.
2. Maybe some of java instruction can't work, need test
3. some of java instruction not implementation , see MV.java
4. Object memory allocation 

change log:
1. Add base class java.lang.*, java.io.PrintStream
2. Add String to handle text output, StringBuilder to handle string concat
3. Trace instruction flow , to fix register var scope bug.




=================================
class2ir readme

This project is the compiler from class files (Java byte code) to LL files (LLVM IR assembler).
Result files can be compiled by llvm-as to standalone binary ELF files.

Features:

* No JDK, no JVM
* Linux x86_64 target arch
* Extreme small size (~10-20 kB ordinary program)
* Use glibc
* Use clang for system object

At this moment project in active development, many things does not work.
