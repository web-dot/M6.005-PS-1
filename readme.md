## About the problem set

Every problem set has two submission points: a beta submission and a final submission. The initial release of the problem set (e.g., this page about Problem Set 1) includes tests for the beta submission. After the beta deadline passes, additional tests will be released for you to download from edX. You can then run these final tests against your solution, fix any new problems that are found, and then submit your revised program for the final deadline.<br />


For the problem sets, all the test cases are given to you, and you'll run the tests on your own machine before uploading your problem set, so you'll always know which tests are passing and which are failing before you submit. There are no hidden tests for the problem sets. You'll get checked off for the beta submission if it passes most of the beta tests (typically at least 80-85%), and you'll get checked off for the final submission if it passes most of the beta + final tests.


## Problem Set 1: Getting Started


#### Overview

The purpose of this problem set is to:

1]introduce the tools we use in 6.005x, including Java, Eclipse, and JUnit;<br />
2]introduce the process for 6.005x problem sets;<br />
3]and practice reading a function specification and writing basic Java to implement it.<br />

You should focus in this problem set on writing code that is safe from bugs and easy to understand, using the techniques we discuss in class. You won't be asked to write any test cases of your own on this problem set. Testing will happen in Problem Set 2.

In the Eclipse Package Explorer, open up ps1-warmup / src / ps1, and you should find the file Quadratic.java. Your warm-up task is to implement the roots() method in this class, which finds the roots of a quadratic equation. The method's specification comment describes how it should behave. Pay close attention to this specification while you're implementing. The quadratic formula will be useful in your solution, but be careful! Many things can go wrong.

Before you start writing code, read the rest of this handout, because it describes three ways that you can use to check your implementation: (1) a main method, (2) a JUnit test suite, and (3) an autograder. Read about and try running each of these first, using the unfinished roots() implementation that we provided you, and then come back and start working on your implementation.

## Running main()

The Quadratic class also contains a main method. The method public static void main(String[] args) is the standard entry point for a Java program. In this case, the main method calls roots() on a simple quadratic equation.

To run main, right-click on Quadratic.java in the Package Explorer, and choose Run As → Java Application. You will see the results printed in the Console tab at the bottom of the Eclipse window. It will say "not implemented yet" if you haven't started writing roots()

## Run JUnit Tests

A main method is not a great way to test a program. Much better is automated unit testing, which runs a suite of tests to automatically test whether the implementations are correct.

JUnit is a widely-adopted Java unit testing library, and we will use it heavily in 6.005.

To find the tests for Quadratic, open up ps1-warmup/test/ps1 in the Package Explorer, where you should find the file QuadraticTest.java. By convention, JUnit tests are put in a class whose name ends in Test, and 6.005 goes a step further by putting them in the test/ folder rather than the src/ folder.

To run the tests, right click on QuadraticTest.java in the Package Explorer, and choose Run As → JUnit Test. You should see the JUnit view appear.

If your implementation of roots() is correct, you should see a green bar, indicating that all the tests passed.

If your implementation is still broken or unfinished, you should see a red bar, and a list of the tests that were run. Clicking on a test shows a stack trace in the bottom box, which provides a brief explanation of what went wrong. Double-clicking on a line in the stack trace goes to the code for that frame in the trace. This is most useful for lines that correspond to your code; this stack trace will also contain lines for Java libraries or JUnit itself.

Use these tests to help you implement roots().

## Run the Autograder

Once your implementation is passing all the JUnit tests, you need to run the automatic grader. The autograder is the file grader.xml in your project. It is written as an Ant script, where Ant is an example of a build management tool, a kind of tool commonly used in software development to compile code, run tests, and package up code for deployment. Our autograder script does all three of these things. Support for running Ant scripts is built into Eclipse.

To run the automatic grader, right click on grader.xml in the Package Explorer, and choose Run As → Ant Build. Choose the plain Ant Build rather than Ant Build..., because you don't need all the options that the Ant Build... dialog box will offer you.

The grading script will run and display output in the Console tab. At the end, it should tell you that it has created two new files: my-grader-report.xml, which is the result of running the grading tests, and my-submission.zip, which is your problem set code and grader output packaged up and ready for submission to edX.

Note: if automatic workspace refreshing is not working for some reason, then my-grader-report.xml and my-submission.zip may not immediately appear in the Eclipse Package Explorer. Try refreshing the project manually by right-clicking on ps1-warmup and choosing Refresh. Then you should see the files appear. If they still aren't there, check the Console tab for errors.
To view your autograder results, double-click on my-grader-report.xml, and you will see the results in your JUnit pane. The my-grader-report.xml file is simply the output of running JUnit on the autograder's tests. For now (Problem Set Beta 1), the autograder tests are identical to the tests you've already been using in QuadraticTest.java, so you should see exactly the same tests passing or failing that you see when you ran JUnit yourself as in the previous section. On future problem sets, the autograder will run different tests.

You can change your code and rerun the autograder as often as you want. You have to double-click on my-grader-report.xml each time to see the newest results. You don't need to Refresh the project each time, however. Once my-grader-report.xml is visible in the Package Explorer, Eclipse will load the latest version whenever you click on it.


## Course Staff
## Rob MIller
Rob Miller
Professor, Computer Science MIT
