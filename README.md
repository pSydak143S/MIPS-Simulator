# MIPS-5-Stage-Pipelined-Processor
This project is a C++ implementation of a 5-stage MIPS processor with pipelining. The simulator accurately models the execution of instructions in each pipeline stage. It supports a subset of the MIPS instruction set and operates with cycle accuracy. The program takes input from a text file named "imem.txt" to initialize the Instruction Memory. Each line in the file represents a byte stored in the Instruction Memory in binary format. The memory is organized in a Big-Endian format, with the most significant byte stored first. The Data Memory is initialized using another text file named "dmem.txt," following the same format as the Instruction Memory.

The MIPS pipeline consists of five stages:

Fetch (IF): This stage retrieves an instruction from the Instruction Memory and updates the Program Counter (PC).

Decode (ID/RF): In this stage, the instruction is decoded, and the necessary control signals for subsequent stages are generated. Additionally, branch instructions are resolved by evaluating the branch condition and calculating the effective address.

Execute (EX): This stage performs the required Arithmetic Logic Unit (ALU) operation.

Memory (MEM): Here, the processor loads or stores a 32-bit word from the Data Memory.

Writeback (WB): In the final stage, the processed data is written back to the Register File (RF).
