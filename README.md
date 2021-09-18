---
description: For INT101 SIT KMUTT
---

# Java Basic

## Data Type

### Primitive Data type

* boolean         \(ture, false\)
* char                \(one char\)
* byte                \(In the range of -128 to 127\)
* short              \(in the range of -32768 to 32767 \| 2 bytes\)
* int                   \(in the range of -2,147,483,648 to 2,147,483,647 \| 4 bytes\)
* long                \(in the range of -9,223,372,036,854,775,808 to 9,223,372,036,854,775,807 \| 8 bytes\)
* float                \(storing 6 to 7 decimal digits \| 4 bytes\)
* double            \(storing 15 decimal digits \| 8 bytes\)

### Reference Data type

* Class

## Operator

### Arithmetic operators

* +
* -
* \*
* /
* %

### Compound assignment

* +=
* -=
* \*=
* /=
* %=
* &gt;&gt;=
* &lt;&lt;=
* &=
* ^=
* \|=

### Increment and decrement

* ++  \(prefix\)
* ++  \(postfix\)
* --     \(prefix\)
* --     \(postfix\)

```text
public class IncrementDecrement {
    public static void main (String[] atgs) {
        int i = 1;
        int j = 1;
        System.out.println("++i = " + (++i));
        System.out.println("j++ = " + (j++));
        
        System.out.println("++i = " + (--i));
        System.out.println("j++ = " + (j--));
    }
}
```

### Relational and comparison operators

* ==
* !=
* &lt;
* &gt;
* &lt;=
* &gt;=

### Logical operators

* !
* &&
* \|\|

## Condition

### if

```text
if (expression) {
    statements
}
```

### If else

```text
public class IfElseStatement {
    public static void main(String[] args) {    
        String username = "user";
        String password = "123456";

        if (username == "user" && password == "123456") {
            System.out.println("You're now logged in.");
        } else {
            System.out.println("Sorry, your usename or password is incorrect.");
        }  
    }
}
```

### Else-If

```text
public class demo {
    public static void main(String[] args) {
        int score = 10;
        if(score >= 80){
            System.out.println("A");
        }else if(score >= 70){
            System.out.println("B");
        }else if(score >= 60){
            System.out.println("C");
        }else if(score >= 50){
            System.out.println("D");
        }else{
            System.out.println("F");
        }
    }
}
```

### Nested If-Else

```text
if ( expression ) {
    // nested level 1
    if ( expression) {
        // nested level 2
        if ( expression) {
            ...
        }
    }
} else {
    // nested level 1
    if ( expression) {

    }
}
```

### Switch

```text
import java.util.Scanner;

public class demo {
    public static void main(String[] args) {
        Scanner reader = new Scanner(System.in);
        System.out.print("What\'s floor do you want to go: ");
        char floor = reader.next().charAt(0);

        switch (floor) {
            case 'G' :
                System.out.println("Elevator is going to ground floor.");
                break;
            case '1' :
                System.out.println("Elevator is going to first floor.");
                break;
            case '2' :
                System.out.println("Elevator is going to second floor.");
                break;
            case '3' :
                System.out.println("Elevator is going to third floor.");
                break;
            default:
                System.out.println("Elevator don't know where to go.");
        }
    }
}
```

### Ternary Operator

```text
variable = Expression1 ? Expression2: Expression3
```

```text
if(Expression1)
{
    variable = Expression2;
}
else
{
    variable = Expression3;
}
```

```text
import java.io.*;
 
class Ternary {
    public static void main(String[] args)
    {
 
        // variable declaration
        int n1 = 5, n2 = 10, max;
 
        System.out.println("First num: " + n1);
        System.out.println("Second num: " + n2);
 
        // Largest among n1 and n2
        max = (n1 > n2) ? n1 : n2;
 
        // Print the largest number
        System.out.println("Maximum is = " + max);
    }
}
```

## Loop

### While loop

```text
public class WhileLoop {
    public static void main(String[] args) {       
        int i = 1;

        while ( i <= 10 ) {
            System.out.print (i  + ", ");
            ++i;
        }     

        System.out.println("End");
    }
}
```

### Do-While loop

```text
import java.util.Scanner;

public class DoWhileLoop {
    public static void main(String[] args) {       
        Scanner reader  = new Scanner(System.in);
        int number;

        System.out.println("\tDetermine odd/even program");

        do {
            System.out.print("Enter odd number to exit loop: ");
            number = reader.nextInt();

            if (number % 2 == 0) {
                System.out.println("You entered " + number + ", it's even.");
            } else {
                System.out.println("You entered " + number + ", it's odd.");
            }

        } while (number % 2 == 0);

        System.out.println("Exited loop.");

    }
}
```

### For loop

```text
public class ForLoop {
    public static void main(String[] args) {
        for (int i = 1; i <= 10; i++) {
            System.out.println("Loop " + i);
        }
        System.out.println("End of loop");
    }
}
```

### Nested For loop

```text
public class ForLoop {
    public static void main(String[] args) {
        int width = 6;
        int height = 6;

        System.out.println("\tMatrix program");
        for (int i = 1; i <= height ; i++) { 
            for (int j = 1; j <= width ; j++) {
                System.out.print("\t" + (i * j));
            }
            System.out.println();
        }
    }
}
```

### Continue

```text
public class ContinueStatement {
    public static void main(String[] args) {

        for (int i = 10; i >= 1; i--) {
            if (i == 5) {
                continue;
            }
            System.out.print(i + ", ");
        }
        System.out.println(" End");
    }
}
```

### Break

```text
public class BreakStatement {
    public static void main(String[] args) {     
        int i = 1;

        while (i <= 10) {       
            if (i == 7) {
                break;
            }
            System.out.print(i + ", ");
            ++i;
        }
        System.out.println(" End");
    }
}
```

## Method

```text
type name ( parameter1, parameter2, ... ) {
    statements
}

access_modifier type name ( parameter1, parameter2, ... ) {
    statements
}
```

> **type** เป็นประเภทของเมธอดที่จะสร้างขึ้น โดยสามารถเป็นได้ทั้ง primitive datatype หรือ reference types ได้ และถ้าหากเมธอดไม่มีการส่งค่ากลับจะใช้คำสั่ง `void`
>
> **name** เป็นชื่อของเมธอดหรือ identifier ซึ่งมีกฏในการตั้งชื่อเช่นเดียวกันกับตัวแปร
>
> **parameters** เป็นลิสต์ของตัวแปรที่จะส่งเข้าไปใช้ในเมธอด โดยสามารถมีตั้งแต่ 1 ขึ้นไปหรือไม่มีก็ได้
>
> **access\_modifier** เป็นการกำหนดระดับการเข้าถึงของเมธอด ซึ่งจะอยู่ในเรื่องของออบเจ็ค โดยมี 4 แลลคือ `private` `protected` `public` และ default \(ไม่ต้องกำหนด\)

 **Argument and Parameter**

```text
public class Example {
  
    public static int multiply(int a, int b)
    {
        return a + b;
    }
  
    public static void main(String[] args)
    {
        int x = 2;
        int y = 5;
  
        // the variables x and y are arguments
        int sum = multiply(x, y);
  
        System.out.println("SUM IS: " + sum);
    }
}
```

```text
public class Example {
  
    // the variables a and b are parameters
    public static int multiply(int a, int b)
    {
        return a + b;
    }
  
    public static void main(String[] args)
    {
        int x = 2;
        int y = 5;
  
        int sum = multiply(x, y);
  
        System.out.println("SUM IS: " + sum);
    }
}
```

### Return

```text
public class MethodReturn {
    public static void main(String[] args) {

        float pi = getPI();
        System.out.println("Value of PI is " + pi);

        System.out.println("\nDetemine if the number is or not");
        for (int i = 1; i <= 20; i++) {
            if (isPrime(i)) {
                System.out.println(i + " is prime");
            } else {
                System.out.println(i + " is not prime");
            }
        }

    }

    public static float getPI () {
        return 3.14f;
    }

    public static boolean isPrime(int number) {
        for (int i = 2; i < number; i++) {
            if (number % i == 0 && i != number) return false;
        }
        return true;
    }   
}
```



