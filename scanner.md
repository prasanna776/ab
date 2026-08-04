# 📖 Java Scanner Example - Reading User Input

This example demonstrates how to use the `Scanner` class in Java to read different types of user input from the keyboard.

---

# 💻 Java Program

```java
import java.util.Scanner; // 1. Import the Scanner class

public class Main {

    public static void main(String[] args) {

        // 2. Create a Scanner object for keyboard input
        Scanner scanner = new Scanner(System.in);

        // 3. Read a String (Full Line)
        System.out.print("Enter your full name: ");
        String name = scanner.nextLine();

        // 4. Read an Integer
        System.out.print("Enter your age: ");
        int age = scanner.nextInt();

        // 5. Read a Double (Decimal)
        System.out.print("Enter your GPA: ");
        double gpa = scanner.nextDouble();

        // 6. Display the captured inputs
        System.out.println("\n--- User Profile ---");
        System.out.println("Name: " + name);
        System.out.println("Age: " + age);
        System.out.println("GPA: " + gpa);

        // 7. Close the scanner to release resources
        scanner.close();
    }
}
```

---

# 📚 Step-by-Step Explanation

## 1️⃣ Import the Scanner Class

```java
import java.util.Scanner;
```

### Explanation

- `Scanner` is a predefined class in the `java.util` package.
- It allows a Java program to read input from different sources.
- Here, it is used to read input from the keyboard.

---

## 2️⃣ Create a Scanner Object

```java
Scanner scanner = new Scanner(System.in);
```

### Explanation

- `Scanner` is a class.
- `scanner` is an object of the Scanner class.
- `new Scanner(System.in)` creates a Scanner object.
- `System.in` represents the keyboard input stream.

### Syntax

```java
Scanner objectName = new Scanner(System.in);
```

---

## 3️⃣ Read a String (Full Line)

```java
System.out.print("Enter your full name: ");
String name = scanner.nextLine();
```

### Explanation

- Displays a message asking the user to enter their name.
- `nextLine()` reads the entire line until the Enter key is pressed.

### Example Input

```
John David Smith
```

### Stored Value

```
John David Smith
```

---

## 4️⃣ Read an Integer

```java
System.out.print("Enter your age: ");
int age = scanner.nextInt();
```

### Explanation

- `nextInt()` reads an integer value.
- The entered value is stored in the variable `age`.

### Example Input

```
22
```

### Stored Value

```
22
```

---

## 5️⃣ Read a Double

```java
System.out.print("Enter your GPA: ");
double gpa = scanner.nextDouble();
```

### Explanation

- `nextDouble()` reads a decimal number.
- The value is stored in the variable `gpa`.

### Example Input

```
8.75
```

### Stored Value

```
8.75
```

---

## 6️⃣ Display the Values

```java
System.out.println("\n--- User Profile ---");
System.out.println("Name: " + name);
System.out.println("Age: " + age);
System.out.println("GPA: " + gpa);
```

### Explanation

Displays all the values entered by the user.

### Sample Output

```
--- User Profile ---
Name: John David Smith
Age: 22
GPA: 8.75
```

---

## 7️⃣ Close the Scanner

```java
scanner.close();
```

### Explanation

- Closes the Scanner object.
- Releases the system resources associated with it.
- It is a good programming practice to close the Scanner after use.

---

# 📝 Sample Execution

### Input

```
Enter your full name: Prasanna Komati
Enter your age: 20
Enter your GPA: 8.9
```

### Output

```
--- User Profile ---
Name: Prasanna Komati
Age: 20
GPA: 8.9
```

---

# 📌 Scanner Methods Used

| Method | Description | Example Input | Returns |
|---------|-------------|---------------|----------|
| `nextLine()` | Reads a complete line of text | Prasanna Kumar | String |
| `nextInt()` | Reads an integer | 25 | int |
| `nextDouble()` | Reads a decimal number | 8.75 | double |

---

# ⚠️ Important Note

If you use `nextInt()`, `nextDouble()`, or similar methods **before** calling `nextLine()`, the leftover newline character (`\n`) from pressing **Enter** remains in the input buffer. As a result, the following `nextLine()` may read only that newline and return an empty string.

Example:

```java
int age = scanner.nextInt();
scanner.nextLine(); // Consume the leftover newline
String name = scanner.nextLine();
```

---

# 🎯 Key Points

- Import the `Scanner` class using `import java.util.Scanner;`.
- Create a Scanner object with `new Scanner(System.in)`.
- Use different Scanner methods to read different data types.
- `nextLine()` reads an entire line of text.
- `nextInt()` reads an integer.
- `nextDouble()` reads a decimal number.
- Close the Scanner using `scanner.close()` when finished.

---

# 📖 Conclusion

The `Scanner` class is one of the easiest ways to accept keyboard input in Java. By using methods like `nextLine()`, `nextInt()`, and `nextDouble()`, you can read different types of data and build interactive console applications.
