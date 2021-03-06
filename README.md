
####Coverage Report
![report](coveragereport/report.JPG)
### Test Generation with Constraints and Mocking

Run `node main.js` to generate `test.js`.  The code under test is `subject.js`.

* 1) Use the `mock-fs` framework to generate a fake file system to help improve coverage.
* 2) Use the `faker` framework to generate a fake phone number to help improve coverage.
* 3) Extend the constraint discovery code to handle `>` and `<`.
* 4) Use clues in the code to automate the process of including file system, phone number mocking without manual injection.

[faker.js docs](https://github.com/Marak/faker.js), [mock-fs docs](https://www.npmjs.com/package/mock-fs)

##### You can see a better visualization of the results here:
    
    open coverage/lcov-report/TestGeneration/subject.js.html

### Test Generation in Java

Download randoop:

    wget https://randoop.googlecode.com/files/randoop.1.3.4.jar

Sample execution to generate tests for all classes in the java.util.Collections namespace (Need Java 7):

    java -classpath randoop.1.3.4.jar randoop.main.Main gentests --testclass=java.util.TreeSet --testclass=java.util.Collections --timelimit=60

This will create a file `RandoopTest.java`, which contains a test driver, and `RandoopTest0.java`, which contains the generated unit tests.

### Coverage in Java

[Emma](http://emma.sourceforge.net/intro.html) is a decent option to collect coverage information form a java program.
