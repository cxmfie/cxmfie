Files necessary to compile the program:
- main.c : main interface of the concurrency simulator, no input is needed
- readerwriter.c: file that implements both reader and writer functions for the reader-writer lock problem

In addition to that the folder must also include readerwriter.h, and scenarios.txt. The first one is a header file that includes init() and deinit() functions to create and destroy semaphores and initializes some key variables, and the second one is a file that contains potential scenarios for the reader-writer simulator.

To compile the program:

1. You can use command "make" and it will compile all the files for you which creates the rwmain executable.
2. Alternatively, you can also try "gcc -o rw main.c -l pthread", to compile the program.

To run the program:

The program can be run with two types of input format
1. For fifo and lru use the following format:
./memsim tracefile nFrames policy quiet/debug

2. For segmented fifo use the following format:
./memsim tracefile nframes policy percentage quiet/debug

where:
-policy: fifo, lru or vms
-percentage: 1-100
-tracefile: name of the tracefile
-nFrames: number of frames to use
- quiet/debug: quiet will just print the stats while debug will print every event that happens

This program was tested and compiled with no warnings under the student cluster
