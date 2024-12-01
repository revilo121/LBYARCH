
# Car Acceleration Calculation (C and x86-64 Assembly)

## Project Overview

This project calculates the acceleration of 10,000 cars based on their initial velocity, final velocity, and the time taken. The program is written in C with an external function implemented in x86-64 assembly for high-performance floating-point arithmetic.

The program runs the assembly function 30 times to compute the acceleration values and then calculates the average execution time. The input data is randomly generated for 10,000 cars, and the results are printed out along with the average execution time.

## Execution Time and Performance Analysis

### Execution Time
The program measures the execution time of the `compute_acceleration` function for 10,000 cars over 30 runs using Windows high-resolution performance counters (`QueryPerformanceCounter`). The average execution time is displayed after all runs have completed.

The average execution time for computing the acceleration of 10,000 cars over 30 runs is approximately **X.XXXXXX seconds** (replace with the actual value you observe during testing).

### Short Performance Analysis
- **High-Resolution Timer**: The use of Windows' high-resolution performance counter allows for accurate timing measurements. This ensures the performance data is not influenced by low timer precision.
- **Efficient Computation**: The use of scalar SIMD registers (`xmm` registers) and SIMD floating-point instructions (`mulsd`, `divsd`, `subsd`, etc.) in the assembly code helps achieve efficient floating-point calculations. This contributes to lower execution times even with a large dataset of 10,000 cars.
- **Average Execution Time Calculation**: Running the function 30 times and calculating the average execution time ensures that any variability due to background processes or other system factors is smoothed out, providing a more reliable measure of performance.

### Compilation and Execution
- **C Compiler**: The project is designed to be compiled using Visual Studio Community 2022.
- **Assembler**: The x86-64 assembly code is compiled using NASM.

To compile and run the project, ensure the `10000.c` file and the assembly file (`asmfunc.asm`) are in the same project. Compile both using Visual Studio, and execute the resulting program to observe the results and average execution time.

### Files
- **10000.c**: The main C file that contains the logic for generating input, calling the assembly function, and calculating the average execution time.
- **asmfunc.asm**: The assembly file containing the function `compute_acceleration`, which computes the acceleration values using SIMD registers and instructions.

## Usage
1. Clone the repository or download the project files.
2. Open the project in Visual Studio Community 2022.
3. Compile the C file (`10000.c`) and the assembly file (`asmfunc.asm`).
4. Run the program to see the results and average execution time.

## License
This project is for educational purposes only.
