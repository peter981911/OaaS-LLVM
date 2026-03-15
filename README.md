# OAAS-LLVM
## Object Code Obfuscation Application using LLVM

## Overview
OAAS-LLVM (Obfuscation As A Service using LLVM) is a software protection tool designed to prevent reverse engineering and unauthorized analysis of compiled programs. The system uses the LLVM compiler infrastructure to transform object files generated from C and C++ programs into heavily obfuscated binaries.

The tool applies multiple obfuscation techniques during compilation to make the final binary significantly more difficult to analyze while preserving the original functionality of the program. The generated binaries are compatible with both Windows and Linux platforms.

This project aims to help developers protect their intellectual property, reduce software piracy, and increase resistance against reverse engineering attacks.

---

## Problem Statement
Modern software applications are vulnerable to reverse engineering through tools such as disassemblers and decompilers. Attackers can analyze compiled binaries to understand program logic, steal proprietary algorithms, bypass license checks, or identify vulnerabilities.

Traditional compilation produces binaries that are relatively easy to analyze using reverse engineering tools. Therefore, there is a need for automated tools that can transform compiled programs into more complex and harder-to-understand forms without affecting their functionality.

OAAS-LLVM addresses this challenge by introducing configurable binary obfuscation techniques using the LLVM framework.

---

## Key Features

- LLVM-based code obfuscation
- Support for C and C++ programs
- Cross-platform binary generation (Windows and Linux)
- Configurable obfuscation levels
- Multiple obfuscation techniques
- Detailed obfuscation report generation
- Protection against reverse engineering

---

## Obfuscation Techniques Used

### Control Flow Obfuscation
Transforms the logical flow of the program into a more complex structure using additional branches, loops, and conditional jumps.

### Bogus Code Insertion
Adds fake instructions and irrelevant computations to confuse static analysis tools.

### String Obfuscation / Encryption
Sensitive strings within the program are encrypted and only decrypted during runtime.

### Fake Function Insertion
Introduces unused functions that appear legitimate but serve no functional purpose, increasing analysis complexity.

### Multi-Cycle Obfuscation
Allows multiple rounds of obfuscation transformations to increase binary complexity.

---

## System Workflow
Source Code Input
↓
Compilation using LLVM
↓
Intermediate Representation (IR)
↓
Obfuscation Passes Applied
↓
Binary Generation
↓
Obfuscation Report Generation


---

## Input

The system accepts:

- C source files (`.c`)
- C++ source files (`.cpp`)

Users can specify parameters such as:

- Obfuscation level
- Number of obfuscation cycles
- String encryption options
- Fake function insertion count

---

## Output

### 1. Obfuscated Binary
A protected executable file for Windows or Linux that maintains original functionality but is difficult to reverse engineer.

### 2. Obfuscation Report
The report includes:

- Input parameters used
- Size of output binary
- Type of obfuscation techniques applied
- Number of bogus code segments generated
- Number of obfuscation cycles performed
- Number of encrypted strings
- Number of fake functions inserted

---

## Technologies Used

- LLVM Compiler Infrastructure
- Clang Compiler
- C / C++
- Python / Shell scripting (for automation)
- Linux build environment

---

## Project Structure
OAAS-LLVM/
│
├── src/
│ ├── obfuscation_pass/
│ ├── string_obfuscator/
│ └── control_flow_transform/
│
├── scripts/
│ └── build_pipeline/
│
├── reports/
│ └── obfuscation_reports/
│
├── examples/
│ └── sample_programs/
│
└── README.md


---

## Use Cases

- Software intellectual property protection  
- Secure software distribution  
- Protection against reverse engineering  
- Malware analysis research  
- Cybersecurity education and research  

---

## Expected Outcome
The project will provide a functional tool capable of transforming regular compiled programs into highly obfuscated binaries using LLVM. The resulting binaries will be significantly harder to analyze using reverse engineering tools while maintaining the original program behavior.

---

## Future Improvements

- GUI interface for configuration
- Integration with CI/CD pipelines
- Advanced virtualization-based obfuscation
- Anti-debugging techniques
- Dynamic runtime protection mechanisms

---

## License

This project is intended for educational and research purposes.
