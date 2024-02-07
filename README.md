# PIC16F887A-CALCI-SEGMENT
This code appears to be written in C for a PIC microcontroller, and it seems to implement a basic calculator functionality with addition, subtraction, multiplication, and division operations. The calculator takes input from push buttons connected to the RB0, RB1, RB2, and RB3 pins. The output is displayed on a 7-segment display connected to the PORTC pins.

Initialization:

Configuration of the I/O ports (TRISC, TRISE, TRISB, TRISD). Initialization of the ANSEL and ANSELH registers to set analog inputs to digital. Main Loop:

The program runs in an infinite loop (while(1)) to continuously monitor the input buttons. Inside the loop, it checks the status of the RB0, RB1, RB2, and RB3 buttons. Button Handling:

The program uses a combination of RB0, RB1, and RB2 buttons to input digits 1 to 9. Depending on the position of RD0, RD1, RD2, and RD3 pins, different digits are displayed on the 7-segment display. Operation Execution:

If RB3 button is pressed in different RDx configurations, it performs different operations: Addition: Sums the first three entered digits. Subtraction: Subtracts the second and third entered digits from the first one. Multiplication: Multiplies the first two entered digits. Division: Divides the first entered digit by the second one. Display Output:

The results of the operations are displayed on the 7-segment display by setting the appropriate values in the PORTC register. Delay Function:

The delay function is used to introduce a delay, creating a visible delay between the operations for better user interaction. Variable Usage:

array: Contains values corresponding to each digit (0-9) in 7-segment display format. num: An array to store the entered digits. add, sub, mult, div: Variables to store the results of addition, subtraction, multiplication, and division operations. temp: Temporary variable used for calculations. Loop Control:

The loop runs until RB0 button is pressed, and then it exits.
