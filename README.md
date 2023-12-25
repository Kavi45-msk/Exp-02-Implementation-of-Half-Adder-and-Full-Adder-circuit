# NAME: KAVI M S
# REFERNCE NUMBER: 23013458

# Exp-03-Implementation-of-Half-Adder-and-Full-Adder-circuit

# Implementation-of-Half-Adder-and-Full-Adder-circuit
### AIM:
To design a half adder and full adder circuit and verify its truth table in Quartus using Verilog programming.

### Equipments Required:
Hardware – PCs, Cyclone II , USB flasher
Software – Quartus prime
Theory
Adders are digital circuits that carry out addition of numbers.

# PROCEDURE
Connect the supply (+5V) to the circuit Switch ON the main switch If the output is 1, then the led glows

### Half Adder
Half adder is a combinational circuit that performs simple addition of two binary numbers. The input variables designate the augend and addend bits; the output variables produce the sum and carry. It is necessary to specify two output variables because the result may consist of two binary digits.

Sum = A’B+AB’ =A ⊕ B Carry = AB
![163552156-a13e5a56-c638-4110-97d9-8896907c8d25](https://github.com/Kavi45-msk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147457752/3e6797d2-4064-4f2a-b129-752f103a15cc)

# PROGRAM
```
module de3hafeez(a,b,sum,carry);
input a,b;
output sum,carry;
xor(sum,a,b);
and(carry,a,b);
endmodule
```

# RTL REALIZATION
![291238403-9aca016b-7128-4d2e-a901-ddaac9a35bec](https://github.com/Kavi45-msk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147457752/52c27ea9-5035-4c57-95a6-726a3120e907)

# TRUTH TABLE
![291240788-11615dbf-2ba8-4e05-9fd9-334496a9e29f](https://github.com/Kavi45-msk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147457752/349a992b-f4f9-43fd-b366-7da7c7f8f50d)

# TIMING DIAGRAM
![291242520-99b728ac-2283-46ac-9177-ea99c810fa18](https://github.com/Kavi45-msk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147457752/d9b5f80a-c443-4184-90e2-f9e96e65b61c)


### Full Adder
Full adder is a digital circuit used to calculate the sum of three binary bits. It consists of three inputs and two outputs. Two of the input variables, denoted by A and B, represent the two significant bits to be added. The third input, Cin, represents the carry from the previous lower significant position. Two outputs are necessary because the arithmetic sum of three binary digits ranges in value from 0 to 3, and binary 2 or 3 needs two digits. The two outputs are sum and carry.
Sum =A’B’Cin + A’BCin’ + ABCin + AB’Cin’ = A ⊕ B ⊕ Cin Carry = AB + ACin + BCin

![image](https://user-images.githubusercontent.com/36288975/163552057-b3547877-6d07-45b4-b7e0-bcfebfad9e1d.png)

# Program:
```
module de3_1(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
xor(sum,a,b,c);
assign carry=a&b|b&c|a&c;
endmodule
```
# RTL realization
![291243116-02586837-ef74-4e96-a02d-4600a635b24b](https://github.com/Kavi45-msk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147457752/7431f1b3-2a88-4938-b3b8-6e621aceea73)

# TRUTH TABLE
![291243734-6f9b5471-6948-4c7f-9864-9075adaf1c7b](https://github.com/Kavi45-msk/Exp-02-Implementation-of-Half-Adder-and-Full-Adder-circuit/assets/147457752/21f3b020-6b7d-4e2d-b204-9ccea072377e)

### Result:

Thus the given logic functions are implemented and their operations are verified using verilog programming.
