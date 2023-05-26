// How to run?

clang++ example.cpp  -Xclang -load -Xclang path/llvm_lto_pass/libBinaryCFI.so -O2

// Don't forget to optimize!

// Follow the nice documentation.

https://groups.google.com/g/llvm-dev/c/DR0O3gTVBuA

// How to run using lld as a lto plugin?

clang++ example1.o example2.o -fuse-ld=lld -Wl,-mllvm=-load=path/llvm_lto_pass/libBinaryCFI.so -O2 -flto

// Compile individual files by simply adding -flto option.
clang++ -flto example1.cpp

Note: This project uses clang-format version 17.