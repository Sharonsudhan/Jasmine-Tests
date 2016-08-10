
Introduction to Jasmine
Jasmine is an open source automated testing framework based on behavior driven development that help test your JavaScript code.It can run and execute on any platform or where ever JavaScript runs. Jasmine doesn't depends on any Browsers, DOM or any other JavaScript framework.But combining Jasmine with frameworks like requireJS and JSCover while testing will help make the tests more effective.

#BDD
Behavior-driven development is a development technique which make use of the combination of Tests driven development and domain driven design. It explains the scenarios in sentences or user stories rather than functional tests. Thus it helps create a development process which developers, business or any stake holders could easily understand. It increases collaboration between developers, testers and analysts by combining the functional,technical activities and sharing project resources.How far Jasmine belongs to BDD classification is a debatable question.

#Setting up Jasmine
Setting up Jasmine is not a hard job. You may download the latest standalone version from here. For setting up a stand alone version all you have to do is to write the test and give proper references to Jasmine library files, tests and the actual script inside the spec runner.Spec runner is an HTML file in which we have to refer jasmine library files, your JavaScript files and jasmine test file in the order they are mentioned. Opening the spec runner will run the rest and you can see the results immediately.
#Writing your first test
Lets say I have a file helloworld.js and I have to write tests for an addNumbers function which accepts 2 numbers and returns its sum .For start writing the tests we have to create a JavaScript file and create a test suite first. I will name that file as helloworldTest.js. Open the file in your favorite editor and start creating tests. First we have to create test suite before the test case. we can have multiple test suites in a file.Below is the code to create a test suite.A test case should reside inside a test suite.
describe(“test suite name”,function(){
});
Here describe is the function used to create a test suite. Inside the test suite first parameter is the test suite name in quotes.This should specify the purpose of the test suite. After that inside the call back of that function we can start writing the test.
describe(“Addition specs”,function(){
  it(“should add 2 valid numbers and returns valid result”,   function(){
   expect(addNumbers(1,1)).toEqual(2);
   });
});
Now to run this, include the jasmine library files and source file and then the test file to the spec runner and open the file.This will run the test and show you the result in a user friendly page.
<title>Spec Runner</title>

  <!-- load jasmine -->
  <link rel="stylesheet" type="text/css" href="tools/Jasmine/jasmine.css">
  <script type="text/javascript" src="tools/Jasmine/jasmine.js"></script>
  <script type="text/javascript" src="tools/Jasmine/jasmine-html.js"></script>

  <!-- include source files here... -->
  <script type="text/javascript" src="src/HelloWorld.js"></script>

  <!-- include spec files here... -->
  <script type="text/javascript" src="specs/HelloWorldTest.js"></script>
  
  
