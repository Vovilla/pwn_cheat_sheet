# pwn_cheat_sheet

gdb:

context - gef hints

info proc map - process map

find 0x10, 0x100, 0x3 - find 0x3 in addres space between 0x10 and 0x100

x/8xb 0x1000 - print 8 bytes in hex starting from 0x1000

x/8xw 0x1000 - print 8 words (word is 4 bytes for x64) in hex starting from 0x1000

x/s 0x1000 - print string starting from 0x1000

p/x 0x100 - 0x10 - print result of sub in hex

registers have a memory address 

gef➤  info registers 
eax            0xffffc933          0xffffc933
ecx            0xffffffff          0xffffffff
edx            0xffffc933          0xffffc933
ebx            0x804a000           0x804a000
esp            0xffffc920          0xffffc920
ebp            0xffffcd28          0xffffcd28
esi            0x80486c0           0x80486c0
edi            0xf7ffcba0          0xf7ffcba0
eip            0x80486a3           0x80486a3 <main+208>
eflags         0x296               [ PF AF SF IF ]
cs             0x23                0x23
ss             0x2b                0x2b
ds             0x2b                0x2b
es             0x2b                0x2b
fs             0x0                 0x0
gs             0x63                0x63
gef➤  x/s 0xffffc933
0xffffc933:     'A' <repeats 31 times>, "\220\367Q\236\375\367\027\351\301", <incomplete sequence \367>

int 0x80 is the assembly language instruction that is used to invoke system calls in Linux on x86 (i.e., Intel-compatible) processors.

EDI is used to hold the destination index, ESI holds the source index and EBX is used as a general purpose index register.


libc is under path /lib/x86_64-linux-gnu/libc.so.6






links:

https://defuse.ca/online-x86-assembler.htm     - online x86 assembler
