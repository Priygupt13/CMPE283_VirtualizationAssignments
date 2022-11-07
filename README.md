
CMPE283 : Virtualization Technology

Assignment 1: Discovering VMX Features

Student names: Priya Gupta , Phani Sai Phalli

University Name: San Jose State University

Prerequisites

You will need a machine capable of running Linux, with VMX virtualization features exposed.
You may be able to do this inside a VM, or maybe not, depending on your hardware and software configuration. • You will need at least one github account (create one at github.com if you don’t already have one)

Assignment Details

We studied Intel SDM provided by professor and listened to the lecture provided by professor on this assignment.

1 . Configuare a GCP vm that has the VMX enable
2. Download the cmpe283-1.c source file and Make file from canvas
3. make sure to have make tool and gcc compiler on your VM
4. run(all commands are run in terminal)
    sudo apt install gcc make
5. There are 5 total features that we are trying to detect base on our GCP VM.  
   a. Pinbased (provided by professor Mike as codebase)
   b. Procbased(Primary Proc based), Procbased02 (Secondary Proc based), Procbased03 (Tertiary Proc baseed), exit,entry (write strcuts for these five base on MSR index, and info on SDM, Volume 3 ch.24)
   
   c. Run under the same directory with MakeFile and cmpe283-1 file in terminal
     er_priyagupta123@vt-assignment1:~/cmpe283-1$ make
     After running make command, couple of files .o/.ko files will be generated
   d. use insmod/rmmod tool to insert and remove module
     sudo insmod ./cmpe283-1.ko
     sudo rmmod ./cmpe283-1.ko  
 6.  Use dmesg tool to print
    run -> sudo dmesg
    
 7. By here we sould be able to see the message outputs for pinbased, procbased, procbased02, exit, entry, procbased03 features on terminal
    
   
     
   


