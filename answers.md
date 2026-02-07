# CECS 326 Reading Assignment: Introduction to Operating Systems

## Name
- Jason Sin



## 1. What are the two main functions of an operating system?
An operating system has 2 main functions being providing users with an extended machine. The second function would be the machine has to manage the I/O devices and other system resources.


## 2. What is the difference between timesharing and multiprogramming systems?
In a timesharing system, multiple users are able to access and perform computations on a computing system simultaneously using their own terminal. As compared to Multiprogramming systems, which allow a user to run multiple programs simutaneously. All timesharing systems are multiprogramming systems but not all multiprogramming systems are timesharing systems.

## 3. What family-of-computers idea was introduced in the 1960s with the IBM System/360 mainframes. Is this idea now dead as a doornail or does it live on?
The idea is still alive, as Intel makes Core i3, i5, and i7 CPUs with a multitude of different properties including speed and power consumption. All the machines are architecturally compatible, only differing in price and performance, which is the center of the family idea.

## 4. What is the difference between kernel and user mode? Explain how having two distinct modes aids in designing an operating system.
On kernel mode, the CPU can execute every instruction in its instruction set and use every feature of the hardware when executing. When in user mode, it can execute only a subset of instructions and use only subset of features when executing. The ability to have two modes allows designers to run user programs in user mode preventing them from accessing important instructions.

## 5. On early computers, every byte of data read or written was handled by the CPU (i.e., there was no DMA). What implications does this have for multiprogramming?
The implications this had for multiprogramming was to have the CPU handle very byte transferred between memory and devices. So this meant that the CPU spent most of its time performing I/O instead of executing programs. This resulted in multiprogramming being less effective as the CPU was unable to efficiently switch tasks while waiting for data transfers.

## 6. There are several design goals in building an operating system, for example, resource utilization, timeliness, robustness, and so on. Give an example of two design goals that may contradict one another.
Fairness and real time would be an example. Fairness woudl require that each process be distributed equally, with no process receiving more than its fair share. This contradicts real time as in real time, resources must be distributed according to the deadlines for various activities. This means a disproportionate amount of resources might be allocated to a reail time process.

## 7. Which of the following instructions should be allowed only in kernel mode? (a) Disable all interrupts. (b) Read the time-of-day clock. (c) Set the time-of-day clock. (d) Change the memory map.
Answers a, c, and d should be limited to kernel mode

## 8. Consider a system that has two CPUs, each CPU having two threads (hyperthreading). Suppose three programs, P0, P1, and P2, are started with run times of 5, 10 and 20 msec, respectively. How long will it take to complete the execution of these programs? Assume that all three programs are 100% CPU bound, do not block during execution, and do not change CPUs once assigned.
Depending on how the operating system schedules them, these appilications may take 20, 25, or 30 msec to execute. It would take 20 msec if P0 nad P1 are scheduled on the same CPU and P2 is planned on a different CPU. If P1 is planned on one CPU and P0 and P2 are scheduled on the same CPU then it would take 25 msec. If P1 and P2 are scheduled on the same CPU and P0 is scheduled on the other CPU, it will take 30 msec. If all three are on the same CPU, it will take 35 msec.

## 9. What is a trap instruction? Explain its use in operating systems.
In a trap instruction the CPUs execution mode is changed form user mode to kernel mode. A user program can use this instruction to call operating system kernel functions.

## 10. Modern operating systems decouple a process address space from the machine's physical memory. List two advantages of this design.
The two advantages of the design is that it makes it possible to load an executable program in several locations within the machine's memory during separate runs. It also permits programs to be larger than the machine's memory.