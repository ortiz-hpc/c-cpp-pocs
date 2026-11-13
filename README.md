# pocs-c-cpp

A collection of low-level exercises and Proofs of Concept written in Modern C (C11/C17) and C++ (C++17/C++20).

## 1. Foundations & Memory Management
- Raw pointer arithmetic, stack vs. heap allocation, and scope lifecycle
- Manual memory management (`malloc`/`free`, `new`/`delete`) and RAII principles
- Custom data structures (dynamic arrays, contiguous memory buffers)
- Reference vs. pointer semantics and const correctness

## 2. Low-Level Architecture & Performance
- Cache locality, memory alignment, and matrix layout optimization (row-major vs. column-major)
- Bit manipulation, inline assembly considerations, and profiling hooks
- Move semantics, perfect forwarding, and zero-cost abstractions (C++)

## 3. Concurrency & Parallelism
- Multi-core CPU exploitation using **OpenMP** (parallel loops, reduction, work-sharing)
- Distributed computing foundations using **MPI** (message passing, point-to-point, collective operations)
- Thread safety, synchronization primitives (mutexes, atomics), and race condition avoidance

## 4. Interoperability & Bridge Layer
- Consuming and wrapping external Fortran routines via `extern "C"` and ISO C bindings
- Exposing C/C++ shared libraries (`.so` / `.dll`) to Python using `ctypes`, `cffi`, or `pybind11`
- Zero-copy data sharing between C++ buffers and Python numpy arrays

---

## Requirements & Compilation
- **Compilers:** `gcc` / `g++` (GCC 10+) or `clang` / `clang++`
- **Libraries:** OpenMP runtime, MPI implementation (e.g., OpenMPI)
- **Build System:** Standard `Makefile` or `CMake` per module

```bash
g++ -O3 -Wall -Wextra -std=c++17 -fopenmp source.cpp -o program
./program
