# Java Project Template

This is a template Java project that can be used as a reference for starting new projects. It includes a simple directory structure and build/run commands.

## Project Structure

```
project-root/
│
├── bin/                    # Compiled Java classes
│
├── lib/                    # External libraries
│   ├── junit-4.13.2.jar    # JUnit library
│   └── hamcrest-core-1.3.jar  # Hamcrest library (required by JUnit)
│
└── src/                    # Source code
    └── test/               # Test source code
        └── com/            # Test package
            └── abccompany/ # Test package
                └── AppTest.java  # Example test file
```

## Build Command

To compile the project, use the following command:

```bash
javac -d bin ./src/test/com/abccompany/AppTest.java -cp ./lib/junit-4.13.2.jar
```

This command compiles the `AppTest.java` file located in `./src/test/com/abccompany/` directory and places the compiled classes in the `bin` directory. It also includes the JUnit library in the classpath.

## Run Command

To run the tests, use the following command:

```bash
java -cp .:./lib/junit-4.13.2.jar:./lib/hamcrest-core-1.3.jar:./bin org.junit.runner.JUnitCore test.com.abccompany.AppTest
```

This command executes the JUnit tests using the `org.junit.runner.JUnitCore` class. It includes both the JUnit and Hamcrest libraries in the classpath, as well as the compiled test classes in the `bin` directory.