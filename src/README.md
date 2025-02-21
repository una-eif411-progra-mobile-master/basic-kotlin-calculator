# Universidad Nacional de Costa Rica
## Escuela de Informática
### EIF411 - Diseño y Programación de Aplicaciones Móviles
#### Práctica de Laboratorio: Calculadora básica en Kotlin

**Profesor:** Maikol Guzmán Alán

---

# Basic Kotlin Calculator Exercise

## Learning Objectives
- Create a simple calculator using Kotlin
- Implement basic arithmetic operations
- Write unit tests for the calculator functions
- Practice Kotlin programming fundamentals

## Requirements

### Calculator Implementation
Create a Calculator class that:
- Performs basic arithmetic operations (add, subtract, multiply, divide)
- Handles basic error cases (like division by zero)
- Returns results as Double values

### Unit Testing
Write tests to verify:
- All basic arithmetic operations work correctly
- Error cases are properly handled
- Edge cases (like large numbers) are managed appropriately

## Implementation Steps

1. Create the Calculator Class:
```kotlin
class Calculator {
    fun add(a: Double, b: Double): Double {
        // TODO: Implement addition
    }

    fun subtract(a: Double, b: Double): Double {
        // TODO: Implement subtraction
    }

    fun multiply(a: Double, b: Double): Double {
        // TODO: Implement multiplication
    }

    fun divide(a: Double, b: Double): Double {
        // TODO: Implement division
    }
}
```

2. Create Test Class:
```kotlin
class CalculatorTest {
    private lateinit var calculator: Calculator

    @BeforeEach
    fun setUp() {
        calculator = Calculator()
    }

    // TODO: Add test methods
}
```

## Example Usage

Your calculator should support basic usage like this:

```kotlin
val calculator = Calculator()
val sum = calculator.add(5.0, 3.0)      // Returns 8.0
val difference = calculator.subtract(10.0, 4.0)  // Returns 6.0
val product = calculator.multiply(2.0, 3.0)    // Returns 6.0
val quotient = calculator.divide(10.0, 2.0)    // Returns 5.0
```

## Unit Testing Requirements

Create comprehensive unit tests for your calculator. For each operation, you should:

1. Create Test Methods:
    - Name each test method clearly (e.g., `testAdditionPositiveNumbers`, `testMultiplicationWithZero`)
    - Test both positive and negative scenarios
    - Include edge cases

2. Test Categories to Implement:
    - Basic operations with positive numbers
    - Operations with negative numbers
    - Operations with zero
    - Edge cases (very large numbers, very small numbers)
    - Error conditions (like division by zero)

3. Testing Structure:
    - Use descriptive test names
    - Follow the Arrange-Act-Assert pattern
    - Include comments explaining test scenarios

Example test structure (but create your own tests!):
```kotlin
class CalculatorTest {
    private lateinit var calculator: Calculator

    @BeforeEach
    fun setUp() {
        calculator = Calculator()
    }

    // TODO: Create your addition tests
    @Test
    fun testAddition() {
        // Arrange: Set up your test values
        // Act: Perform the calculation
        // Assert: Check the result
    }

    // TODO: Create your subtraction tests
    @Test
    fun testSubtraction() {
        // Implement your test
    }

    // TODO: Create your multiplication tests
    @Test
    fun testMultiplication() {
        // Implement your test
    }

    // TODO: Create your division tests
    @Test
    fun testDivision() {
        // Implement your test
    }

    // TODO: Create error case tests
    @Test
    fun testErrorCases() {
        // Implement your test
    }
}
```

## Evaluation Criteria

Your implementation will be evaluated based on:
1. Correct implementation of arithmetic operations
2. Proper error handling
3. Test coverage and quality
4. Code clarity and organization

## Submission Requirements

Submit:
1. Calculator.kt file with your implementation
2. CalculatorTest.kt file with your unit tests
3. Brief comments explaining any important logic

## Tips for Success

1. Start with simple test cases first
2. Handle division by zero appropriately
3. Consider edge cases like negative numbers
4. Use clear variable names
5. Add comments for complex logic

## Timeline

Suggested time allocation:
- Implementation: 30 minutes
- Unit Testing: 30 minutes
- Documentation: 15 minutes

## Development Environment Setup

You can use either IntelliJ IDEA or Visual Studio Code for this project. Choose the one you're most comfortable with.

### Option 1: Using IntelliJ IDEA

1. Install IntelliJ IDEA:
    - Download IntelliJ IDEA Community Edition (free) from https://www.jetbrains.com/idea/download/
    - During installation, make sure to select "Kotlin" plugin

2. Create New Project:
    - Open IntelliJ IDEA
    - Click "New Project"
    - Select "Kotlin" from the left sidebar
    - Choose "JVM | IDEA" as the project template
    - Set your project name and location
    - Choose JDK 11 or newer
    - Click "Create"

3. Project Structure:
    - Your project will automatically be set up with the correct structure
    - Source files go in `src/main/kotlin`
    - Test files go in `src/test/kotlin`

4. IntelliJ Tips:
    - Right-click on test method names and select "Run" to execute individual tests
    - Use Alt+Enter (Option+Enter on Mac) for quick fixes and suggestions
    - Press Double Ctrl (or Double ⌘ on Mac) to run anything
    - Use "Show Context Actions" (Alt+Enter) for quick code generation

5. Running Tests in IntelliJ:
    - Click the green play button next to your test class
    - Use the Test window to see results
    - Right-click on a test folder to run all tests
    - Use the built-in test coverage tools

### Option 2: Using Visual Studio Code

1. Install Required Software:
    - Install Visual Studio Code from https://code.visualstudio.com/
    - Install Java Development Kit (JDK) 11 or newer
    - Install Kotlin compiler

2. Install VS Code Extensions:
    - Kotlin Language (by Mathias Frolich or fwcd)
    - Test Explorer UI
    - Kotlin Test Explorer
    - Extension Pack for Java

3. Project Setup in VS Code:
    - Create a new directory for your project
    - Open VS Code in that directory
    - Create a new file `build.gradle.kts` with the following content:
   ```kotlin
   plugins {
       kotlin("jvm") version "1.8.0"
   }

   repositories {
       mavenCentral()
   }

   dependencies {
       implementation(kotlin("stdlib"))
       testImplementation(kotlin("test"))
       testImplementation("org.junit.jupiter:junit-jupiter:5.8.2")
   }

   tasks.test {
       useJUnitPlatform()
   }
   ```

4. Project Structure:
   ```
   your-project/
   ├── build.gradle.kts
   ├── src/
   │   ├── main/
   │   │   └── kotlin/
   │   │       └── Calculator.kt
   │   └── test/
   │       └── kotlin/
   │           └── CalculatorTest.kt
   ```

5. VS Code Tips:
    - Use Command Palette (Ctrl+Shift+P or Cmd+Shift+P) to run Kotlin commands
    - Use the Test Explorer to run and debug tests
    - Enable auto-save in VS Code settings
    - Use the integrated terminal for Gradle commands