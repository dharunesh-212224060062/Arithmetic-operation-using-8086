# Arithmetic-operation-using-8086
# 8086 Assembly Language Programs for Arithmetic Operations

## AIM

To write and execute Assembly Language Programs to perform arithmetic operations for the 8086 microprocessor.

---

## APPARATUS REQUIRED

* Personal Computer with MASM Software

---

## 1. ADDITION

#### Algorithm

1. Initialize memory location in HL register.
2. Store 1st data.
3. Increment HL to enter 2nd data.
4. Move 2nd number to accumulator.
5. Decrement HL.
6. Add value in memory with accumulator.
7. Store result.
8. Stop.


## FLOW CHART
<img width="707" height="1024" alt="image" src="https://github.com/user-attachments/assets/b5a7062d-e294-47cd-9683-a40de25e82de" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV CL,00H
MOV AX,[SI]
MOV BX,[SI+02H]
ADD AX,BX
JNC L1
INC CL
L1:
MOV [SI+04H],AX
MOV [SI+06H],CL
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
  
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|     1200 : 12           |      1204 : 24           |
1201 : 34  |  1205 : 68
1202 : 12   | 1206 : 00
1203 : 34    |1207 : C4                       |                          |

#### Manual Calculations

![WhatsApp Image 2025-08-25 at 09 45 33_f613fbf3](https://github.com/user-attachments/assets/bd1835f9-c1f7-4430-ba22-6798766d1862)


---

## OUTPUT IMAGE FROM MASM SOFTWARE
![WhatsApp Image 2025-08-25 at 08 35 19_43078ab0](https://github.com/user-attachments/assets/09322ee2-63bb-4e06-a66b-f146e8ebf73e)


## 2. SUBTRACTION

#### Algorithm

1. Initialize memory and store 1st data.
2. Increment to get 2nd data.
3. Move 2nd data to accumulator.
4. Subtract memory content.
5. Store result.

## FLOWCHART

<img width="578" height="797" alt="image" src="https://github.com/user-attachments/assets/564c3c7a-33ce-4a1c-8920-beb5c24b9b47" />


#### Program



#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|               1200 : 12          |      1204 : 00                    |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : C4
#### Manual Calculations

![WhatsApp Image 2025-08-25 at 09 45 33_3b6c2f52](https://github.com/user-attachments/assets/0406a1bf-38a4-42c0-939b-323a0725a4a9)


---


## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-08-25 at 10 33 54_067fda8f](https://github.com/user-attachments/assets/e9121ede-cc12-49c8-b846-900d2dc3755d)


## 3. MULTIPLICATION

#### Algorithm

1. Initialize memory and store operands.
2. Move operands to registers.
3. Multiply.
4. Store result.

##FLOWCHART

<img width="569" height="906" alt="image" src="https://github.com/user-attachments/assets/88be88ff-2896-4a88-b73d-84ccffd2fcf9" />



#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
MUL BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table
| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|         1200 : 12                |       1204 : 44                   |
1201 : 34 | 1205 : 51
1202 : 12 | 1206 : 97
1203 : 34 | 1207 : 0A


#### Manual Calculations

![WhatsApp Image 2025-08-25 at 09 45 32_0be382c3](https://github.com/user-attachments/assets/7517ee2a-7537-4de4-b91c-a787802defe7)


---

## OUTPUT SCREEN FROM MASM SOFTWARE
![WhatsApp Image 2025-08-25 at 08 36 26_e79f18ab](https://github.com/user-attachments/assets/6ab31f74-0f8e-4c58-b9b1-b6e75fe77780)


## 4. DIVISION

#### Algorithm

1. Load memory location of operands.
2. Perform division.
3. Store result.

   ## FLOWCHART
<img width="1065" height="802" alt="image" src="https://github.com/user-attachments/assets/25b4a483-0d42-494b-8639-1af3ea17191b" />


#### Program

```asm
CODE SEGMENT
ASSUME CS: CODE, DS: CODE
ORG 1000H
MOV SI,2000H
MOV DX,0000H
MOV AX,[SI]
MOV BX,[SI+02H]
DIV BX
MOV [SI+04H],AX
MOV [SI+06H],DX
MOV AH,4CH
INT 21H
CODE ENDS
END
```

#### Output Table

| MEMORY LOCATION (INPUT) | MEMORY LOCATION (OUTPUT) |
| ----------------------- | ------------------------ |
|       1200 : 12                  |              1204 : 01            |
1201 : 34 | 1205 : 00
1202 : 12 | 1206 : 00
1203 : 34 | 1207 : 00


#### Manual Calculations

![WhatsApp Image 2025-08-25 at 09 45 32_7d48fb24](https://github.com/user-attachments/assets/a842d2c0-53ff-4144-9842-662c65c3167a)


---
## OUTPUT FROM MASM SOFTWARE
![WhatsApp Image 2025-08-25 at 10 37 48_4b2e521a](https://github.com/user-attachments/assets/e5a42b41-0b7d-4c6c-b961-0d9e66029af0)



## RESULT

Thus, the Assembly Language Programs for 8086 to perform arithmetic operations (Addition, Subtraction, Multiplication, and Division) using both direct and indirect methods were successfully written and executed using MASM.
