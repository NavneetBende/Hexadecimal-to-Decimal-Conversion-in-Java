# Hexadecimal-to-Decimal-Conversion-in-Java

Hexadecimal to Decimal Conversion
Here we will learn the concept of hexadecimal conversion to decimal also learn to code it in java.

Hexadecimal numbers range [ 0, 15 ]

[ 1, 9 ] same as integer
[ 10, 15 ] as [ ‘A’,  ‘F’ ] 
Java Program for hexadecimal to decimal conversion
Hexadecimal Working :
As discussed in hexadecimal numbers range [ 0, 15 ]. Where [ 0, 9 ] are represented same as integer values but after 9 alphabets are used as shown below :

A = 10
B = 11
C = 12
D = 13
E = 14
F = 15
How To Convert From Hexadecimal to Decimal Manually?
For a user input num. This requires you to know ASCII values, please check the ASCII table here 

To convert a hexadecimal to a decimal manually, you must start by multiplying the hex number by 16. Then, you raise it to a power of 0 and increase that power by 1 each time according to the hexadecimal number equivalent.

We start from the right of the hexadecimal number and go to the left when applying the powers. Each time you multiply a number by 16, the power of 16 increases.

When converting a C9 hexadecimal to a decimal your work should look something like this:

Example :

9 = 9 * (16 ^ 0) = 9
C = 12 * (16 ^ 1) = 192
Then, we add the results.

192 + 9 = 201 
Hexadecimal	1	2	3	4	5	6	7	8	9	A	B	C	D	E	F
Decimal	1	2	3	4	5	6	7	8	9	10	11	12	13	14	15
Java Code
Run
class Main
{
  public static void main (String[]args)
  {

    String hex = "C9";
    System.out.println (convert (hex));
  }
  
  static int convert(String hex){  
    String digits = "0123456789ABCDEF";  
             hex = hex.toUpperCase();  
             int val = 0;  
             for (int i = 0; i < hex.length(); i++)  
             {  
                 char c = hex.charAt(i);  
                 int d = digits.indexOf(c);  
                 val = 16*val + d;  
             }  
             return val;  
  }  

}
Output
Decimal value of C9 is 201
