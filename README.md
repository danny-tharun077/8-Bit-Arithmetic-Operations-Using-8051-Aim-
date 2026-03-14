## Aim:
To perform 8-bit arithmetic operations such as addition, subtraction, multiplication, and division using the 8051 microcontroller.

## Apparatus Required:

•	Laptop with Keil uVision software

## Algorithm:

## For Addition:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Add the contents of registers A and B.
4.	Store the result in memory location 40H.
5.	Store the carry (if any) in 41H.

## Program:
```
  MOV A,30H;
  ADD A,31H;
  MOV 40H,A;
  JNC NEXT ;
  MOV 41H,#01H;
  SJMP END_PROGRAM;
  NEXT:MOV 41H,#00H;
  END_PROGRAM:NOP;
  END
```

## Output:
<img width="1915" height="1007" alt="Screenshot 2026-03-12 194856" src="https://github.com/user-attachments/assets/d4e73d29-66bf-4f50-a8da-8038b9708edd" />
<img width="1916" height="1004" alt="Screenshot 2026-03-12 140241" src="https://github.com/user-attachments/assets/dc699db7-8ba5-4d8d-a465-4578d4d209ca" />
 
## For Subtraction:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Subtract B from A.
4.	Store the result in memory location 40H.

## Program:
```
  MOV A,30H
  SUBB A,31H
  MOV 40H,A
  JNC NEXT 
  MOV 41H,#01H;
  SJMP END_PROGRAM;
  NEXT:MOV 41H,#00H;
  END_PROGRAM:NOP;
  END
```

## Output:
<img width="1919" height="1009" alt="Screenshot 2026-03-12 195112" src="https://github.com/user-attachments/assets/2be9ce13-905b-4300-89cb-b678d6577de4" />
<img width="1919" height="1009" alt="Screenshot 2026-03-12 195127" src="https://github.com/user-attachments/assets/d503d683-488b-44e3-98a8-c61dff1bbedd" />

## For Multiplication:
1.	Load the first number from memory location 30H into register A.
2.	Load the second number from memory location 31H into register B.
3.	Multiply A and B.
4.	Store the lower byte of the result in memory location 40H.
5.	Store the higher byte of the result in memory location 41H.

## Program:
```
  MOV A,30H
  MOV B,31H
  MUL AB
  MOV 40H,A
  MOV 41H,B
  END
```

## Output:
<img width="1919" height="1008" alt="Screenshot 2026-03-12 195923" src="https://github.com/user-attachments/assets/2b35db59-3151-4309-9efd-b82be36e5c05" />
<img width="1917" height="1007" alt="Screenshot 2026-03-12 195937" src="https://github.com/user-attachments/assets/87c14c22-59ac-44f1-b101-59bc859951c4" />

## For Division:
1.	Load the dividend from memory location 30H into register A.
2.	Load the divisor from memory location 31H into register B.
3.	Divide A by B.
4.	Store the quotient in memory location 40H.
5.	Store the remainder in memory location 41H.


## Program:
```
  MOV A, 30H
  MOV B, 31H
  DIV AB
  MOV 40H, A
  MOV 41H, B
  END
```

## Output:
<img width="1918" height="1011" alt="Screenshot 2026-03-12 200305" src="https://github.com/user-attachments/assets/2266d623-0328-4e2e-bff2-e75ae4ceece7" />
<img width="1919" height="1011" alt="Screenshot 2026-03-12 200324" src="https://github.com/user-attachments/assets/f447819e-97ea-41cc-a32e-ae85f7daec55" />

## Result:
The 8-bit arithmetic operations using the 8051 microcontroller have been successfully executed and verified using Keil software.

