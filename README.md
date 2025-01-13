# samsung-riscv
# RISCV INTERNSHIP PROGRAM POWERED BY SAMSUNG AND VSD
The instructor and guide for this internship is KUNAL GHOSH Sir,Founder of VSD.
# BASIC DETAILS
# NAME : MIHAL SUVARNA 
# COLLEGE: SAHYADRI COLLEGE OF ENGINEERING AND MANAGEMENT Mangaluru.
# Email ID: mihalsuvarna@gmail.com,mihal.ec23@sahyadri.edu.in
# TASK 1
C based lab screenshot.
riscv based lab screenshot.
# TASK 2 
The compiled c code screenshot.
the riscv objdump for each optimization level(-O1 and -Ofast).
# TASK 3 INSTRUCTION TYPES 

# 1 Instruction: addi sp, sp, -16
Opcode: 0010011 
Immediate: -16 
Source Register 1 (rs1): sp (x2, 5 bits)
Destination Register (rd): sp (x2, 5 bits)
Function (funct3): 000 (3 bits)
# Breakdown:
Immediate (-16):-16 in 12-bit signed binary is 1111111111110000 (12 bits).
Source Register 1 (rs1) (sp = x2):x2 in binary is 00010 (5 bits).
Destination Register (rd) (sp = x2):x2 in binary is 00010 (5 bits).
Function (funct3):addi has funct3 = 000 (3 bits).
Opcode:addi has an opcode of 0010011 (7 bits).
Machine Code:
**Binary**:
1111111111110000 00010 000 00010 0010011
**Hexadecima**l:0xFFF0A023
# 2 Instruction: sd ra, 8(sp)
Opcode: 0100011 (7 bits)
Immediate: 8 (split into 12 bits)
Source Register 1 (rs1): sp (x2, 5 bits)
Source Register 2 (rs2): ra (x1, 5 bits)
Function (funct3): 011 (3 bits)
# Breakdown:
Immediate (8):8 in 12-bit signed binary is 000000000010 (12 bits).
Immediate [11:5] = 0000000 (7 bits).
Immediate [4:0] = 01000 (5 bits).
Source Register 1 (rs1) (sp = x2):x2 in binary is 00010 (5 bits).
Source Register 2 (rs2) (ra = x1):x1 in binary is 00001 (5 bits).
Function (funct3):For sd, the funct3 value is 011 (3 bits).
Opcode:For sd, the opcode is 0100011 (7 bits).
Machine Code:
**Binary**:0000000 01000 00001 011 00010 0100011
Hexadecimal:0x00030223
# 3 Instruction: li a5, 100
Opcode: 0110111 (7 bits)
Immediate: 0 (split into 20 bits for lui instruction)
Source Register 1 (rs1): Not used in lui
Destination Register (rd): a5 (x15, 5 bits)
Function (funct3): Not applicable for lui
# Breakdown:
Immediate [31:12] (0):0 in 20 bits is 00000000000000000000 (20 bits).
Destination Register (rd) (a5 = x15):x15 in binary is 01111 (5 bits).
Opcode:For lui, the opcode is 0110111 (7 bits).
Machine Code (First Instruction): lui a5, 0x0
**Binary**:00000000000000000000 01111 0110111
Hexadecimal:0x00007037
# 3.1 Instruction: addi a5, a5, 100
Opcode: 0010011 (7 bits)
Immediate: 100 (split into 12 bits)
Source Register 1 (rs1): a5 (x15, 5 bits)
Destination Register (rd): a5 (x15, 5 bits)
Function (funct3): 000 (3 bits)
# Breakdown:
Immediate (100):100 in 12 bits is 0000000001100100 (12 bits).
Source Register 1 (rs1) (a5 = x15):x15 in binary is 01111 (5 bits).
Destination Register (rd) (a5 = x15):x15 in binary is 01111 (5 bits).
Function (funct3):For addi, funct3 = 000 (3 bits).
Opcode:For addi, the opcode is 0010011 (7 bits).
Machine Code (Second Instruction): addi a5, a5, 100
**Binary**:0000000001100100 01111 000 01111 0010011
Hexadecimal:0x00030313
# 4 Instruction: jal ra, 10414
Machine Code **Binary**: 0000001000101110101111000000000000011101111
Machine Code (Hex): 0x0052AFF7
# 5 Instruction: lui a0, 0x21
Machine Code **Binary**: 00000000001000010000000001101111
Machine Code (Hex): 0x000210F3
# 6 Instruction: sub a5, a5, s0
Machine Code **Binary**: 0000000 01100 00101 000 10000 0110011
Machine Code (Hex): 0x00C28233
# 7 Instruction: addiw a5, a5, -1
Machine Code **Binary**: 111111111111 00101 000 00101 0010011
Machine Code (Hex): 0xFFF30313
# 8 Instruction:  mv a0, s0
Machine Code **Binary**: 0000000 00000 10111 000 00000 0110011
Machine Code (Hex): 0x00030233
# 9 Instruction: bnez a5, 10190 <main+0xc>
Machine Code **Binary**: 111110011111 01010 001 01010 1100011
Machine Code (Hex): 0xF7A28563
# 10 Instruction: srai s1, a5, 0x3
Machine Code **Binary**: 000000000011 00101 101 00001 0010011
Machine Code (Hex): 0x003303B3













