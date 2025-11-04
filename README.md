# Process Scheduler Simulator

This project emulates the **scheduling behavior of a single-core processor**, implementing multiple classical CPU scheduling algorithms. It provides a hands-on simulation of how different strategies affect process execution and system performance.

The scheduler reads process data from an input file containing details such as **arrival time**, **priority**, and **burst time**. Based on the user’s selected algorithm, the simulator schedules and executes processes accordingly.

## Supported Scheduling Algorithms

### Highest Priority First (HPF)

* **Description:** Executes the process with the highest priority first.
* **Type:** Non-preemptive (can be extended to preemptive if desired).

### Shortest Remaining Time Next (SRTN)

* **Description:** Always selects the process with the **shortest remaining burst time** for execution.
* **Type:** Preemptive version of the Shortest Job First (SJF) algorithm.

### Round-Robin (RR) with Custom Quantum

* **Description:** Each process is given a fixed **time quantum** (customizable by the user).
* After the quantum expires, the CPU switches to the next ready process.
* **Type:** Preemptive and fair — ideal for time-sharing systems.

## Output Files

After simulation, the scheduler generates detailed output files for analysis:

### `scheduler.log`

* Chronicles the **execution timeline** of each process, including:

  * Start time
  * Stop time
  * Resume time
  * Finish time

### `scheduler.perf`

* Summarizes **performance metrics**, including:

  * CPU Utilization (%)
  * Average Waiting Time
  * Average Turnaround Time (WTA)
  * Standard Deviation of WTA

### `memory.log`

* Tracks **memory allocation and deallocation** for each process throughout the simulation.


## Key Features

* Simulates realistic CPU scheduling behavior.
* Supports both preemptive and non-preemptive algorithms.
* Customizable time quantum for Round-Robin.
* Generates comprehensive performance and timeline reports.
