Pwndocker
=========
A docker environment for pwn in ctf based on **phusion/baseimage**, which is a modified ubuntu 16.04 baseimage for docker

### Usage

	docker run -it \
		--rm \
		-h ${ctf_name} \
		--name ${ctf_name} \
		-v $(pwd)/${ctf_name}:/ctf/work \
		-p 23946:23946 \
		--cap-add=SYS_PTRACE \
		skysider/pwndocker

### included software

- [pwntools](https://github.com/Gallopsled/pwntools)  —— CTF framework and exploit development library
- [peda](https://github.com/longld/peda)  ——Python Exploit Development Assistance for GDB
- [ROPgadget](https://github.com/JonathanSalwan/ROPgadget)  —— facilitate ROP exploitation tool
   [roputils](https://github.com/inaz2/roputils) 	—— A Return-oriented Programming toolkit
- [one_gadget](https://github.com/david942j/one_gadget) —— A searching one-gadget of execve('/bin/sh', NULL, NULL) tool for amd64 and i386
- [angr](https://github.com/angr/angr)   ——  A platform-agnostic binary analysis framework
- [radare2](https://github.com/radare/radare2) ——  A rewrite from scratch of radare in order to provide a set of libraries and tools to work with binary files
- [LibcSearcher](https://github.com/lieanu/LibcSearcher) —— A libc search tool based on leaked function address
   linux_server[64] 	—— IDA 7.0 debug server for linux
     [tmux](https://tmux.github.io/) 	—— a terminal multiplexer
     [ltrace](https://linux.die.net/man/1/ltrace)	—— trace library function call
- [strace](https://linux.die.net/man/1/strace) —— trace system call