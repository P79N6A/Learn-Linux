1）testAdd 测试从 c 调用 asm<br>
2）centos 下按照 elf 32位（汇编用的32位写法，不能按照64位编译），编译出来都是 elf 可执行文件<br>
3）在 mac 下用 gcc 编译的是 mach-o 文件，需要使用 i386-elf-gcc<br>

nasm -f elf32 testAdd-s.asm -o testAdd-s.o<br>
gcc -m32 testAdd-c.c testAdd-s.o -o testAdd.out<br>

1）testSub 测试从 asm 调用 c<br>
2）centos 下按照 elf 32位（汇编用的32位写法，不能按照64位编译），编译出来都是 elf 可执行文件<br>
3）在 mac 下用 gcc 编译的是 mach-o 文件，需要使用 i386-elf-gcc<br>

nasm -f elf32 testSub-s.asm -o testSub-s.o<br>
gcc -m32 testSub-c.c testSub-s.o -o testSub.out<br>

