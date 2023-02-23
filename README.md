# cpu-sim
#Q10:Write an assembly program that reads in integers and adds them together; until a
negative non-zero number is read in. Then it outputs the sum (not including the last
number).


    START1:INP
           SNA
           BUN START2
           BUN END
           
    START2:ADD SUM
           STA SUM
           BUN START1
           
   END:LDA SUM
       OUT
       HLT
       
       
#Q11:Write an assembly program that reads in integers and adds them together; until zero is
read in. Then it outputs the sum.

    START1:INP
           SZA
           BUN START2
           BUN END
           
    START2:ADD SUM
           STA SUM
           BUN START1
           
    END:LDA SUM
        OUT
        HLT
    SUM:data 2 0
    
    
#Write an assembly language program to simulate the machine for following register
reference instructions and determine the contents of AC, E, PC, AR and IR registers in
decimal after the execution:
i. CIR
ii. CIL

cil
    
    
    INP
    OUT
    CIL
    OUT
    HLT
    
 CIR
   
   
    INP 
    OUT
    CIR
    OUT
    HLT
 
 
#Write an assembly language program to simulate the machine for following register
reference instructions and determine the contents of AC, E, PC, AR and IR registers in
decimal after the execution:
i. INC
ii. SPA
iii. SNA
iv. SZE

SPA

    INP
    SPA
    CMA
    OUT
    HLT
    
SNA

    INP
    SNA
    OUT
    HLT
    
SZE

    SZE
    CME
    HLT
    
#Write an assembly language program to simulate the machine for following register
reference instructions and determine the contents of AC, E, PC, AR and IR registers in
decimal after the execution:
i. CLA
ii. CMA
iii. CME
iv. HLT

CLA

    INP
    OUT
    CLA
    OUT
    HLT
    
CMA

    INP
    OUT
    CMA
    OUT
    HLT
    
CME

    CME
    HLT
    
HLT

    HLT
    
#Q6:6. Write an assembly program for simulating following memory-reference instructions.
i. ADD
ii. LDA
iii. STA
iv. BUN
v. ISZ

LDA

    INP
    STA 7
    CLA
    LDA 7
    OUT
    HLT
    
STA

    INP
    STA NUM
    HLT
    
    NUM: .data 10
    
bun 

    INP
    BUN JUMP
    OUT
    JUMP:HLT
    NUM:.data 10
    
isz 

    INP
    STA num
    LOOP:ISZ num
         OUT
         BUN LOOP
         HLT
    num: .data 10
    
    
#q5:Write an assembly program to simulate the following logical operations on two userentered numbers.
i. AND
ii. OR
iii. NOT
iv. XOR
v. NOR
vi. NAND

and

    INP
    STA NUM
    INP
    AND NUM
    OUT
    HLT
    
    NUM: .data 10
    
    
 xor
 
    INP
    STA a
    INP
    STA b 
    CMA
    AND a 
    CMA
    STA C
    LDA a
    CMA
    AND b
    CMA
    AND c
    CMA
    OUT
    HLT
    a: .data 20
    b: .data 20
    c: .data 20
    
nor

    INP
    CMA
    STA 30
    INP
    CMA
    AND 30
    OUT
    HLT
    
NAND

    INP
    STA 28
    INP
    AND 28
    CMA
    OUT
    HLT
    
 #Q3:Write an assembly program to simulate ADD operation on two user-entered numbers.
 
 
    INP
    STA 10 ;store the number in 10th memory location
    INP
    ADD 10
    OUT
    HLT

#Q4:Write an assembly program to simulate SUBTRACT operation on two user-entered
numbers.

    INP
    STA NUM ; NUM is variable
    INP
    CMA
    INC 
    ADD NUM
    OUT
    HLT
    
    NUM:.data 10
    
 
    
    
    
    
