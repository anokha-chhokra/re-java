Read this once before the Part 1 problems, then return to it whenever a problem feels unclear. Type every snippet yourself and change it to see what breaks.

### How Java runs

1. You write source code in a `.java` file.
2. `javac` compiles it to platform-independent bytecode in `.class` files.
3. The JVM loads the bytecode, verifies it, interprets it, and compiles hot methods to machine code with the JIT compiler.

The JDK contains the compiler and tools (`javac`, `jar`, `jshell`, `jcmd`); the JRE is the runtime part only. For quick experiments use `jshell`, or run a single file directly with `java Hello.java`.

```java
public class Hello {
    public static void main(String[] args) {
        System.out.println("Hello, " + (args.length > 0 ? args[0] : "world"));
    }
}
```

A class named `Hello` lives in `Hello.java`. The entry point is `public static void main(String[] args)`. Class names use `PascalCase`, methods and variables use `camelCase`, constants use `UPPER_SNAKE_CASE`, and packages are lowercase.

### Primitive types

| Type | Size | Range or values | Default |
| --- | --- | --- | --- |
| `byte` | 8 bits | -128 to 127 | 0 |
| `short` | 16 bits | -32,768 to 32,767 | 0 |
| `int` | 32 bits | about -2.1 billion to 2.1 billion | 0 |
| `long` | 64 bits | about -9.2 x 10^18 to 9.2 x 10^18 | 0L |
| `float` | 32 bits | about 7 decimal digits of precision | 0.0f |
| `double` | 64 bits | about 15 to 16 decimal digits of precision | 0.0 |
| `char` | 16 bits | one UTF-16 code unit, 0 to 65,535 | '\\u0000' |
| `boolean` | JVM-defined | `true` or `false` | false |

### 1A. Syntax, types, and console I/O

- [ ] **1.01** \[L1\] Print your name, then print the same name in reverse using only `System.out`.
