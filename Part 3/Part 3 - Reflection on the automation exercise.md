# Part 3: Reflection on the automation exercise


* The tests from the 2nd task are automated, black-box, functional tests
	* Automated, non manual - executed by test script, not human
	* Black-box, it doesn't check internal functioning of the system as white-box
	* Functional, it's focused on the functioning of the system ("what software does?")

* White-box testing is usually performed to check quality of the code
	* Most often executed by developers
	* Unit tests are example of white-box testing

* Non-functional testing checks HOW the product works
	* Usually performed after the functional testing
	* It's very hard or impossible to perform non-functional testing manually
	* Performance testing, Security testing, Portability testing...
	* It's very important to have both functional and non-functional testing on the product
	* Not introducing non-functional testing can result with "security leaks", slow, not realible system, some functionalities won't work well across different platforms (devices, browsers...)...
	* It's very time (money) consuming, so it's not smart to wait a later phase of the project in order to introduce it

## Tests scope in terms of testing types

* Smoke - NO
	* The tests I wrote in 2nd task aren't basic functionalities of the system, so I wouldn't say they belong to "Smoke" suite. Smoke should contain only the most basic scenarios and cases such is preview of the products on the home page.
* Sanity - YES
	* Sanity (Build verification or extended smoke) should contain core functionalities of the system, that should work as expected at any time. It should be run frequently, whenever there's a new build integrated, in order to check that these functionalities aren't jeopardized with new code merged. These cases from 2nd task are definitely core functionalities of the system and should be in "sanity" suite.
* Regression - YES
	* Once developed, tested, integrated and released, code should be checked periodically in order to assure everything work as expected. We can say that Sanity testing is a subset of regression testing (the most important one), so these tests should be in "regression" suites. 
* Unit - NO
	* Unit testing is a level of software testing where individual units of a software are tested. A unit is the smallest testable part of any software (like method or just part of it). As already mentioned it's white-box and usually performed by developers. When writing new code, they should cover it by adequate unit tests.
* End-to-end - YES
	* The main purpose of End-to-end testing is to test from the end user’s experience by simulating the real user scenario and validating the system under test. Software systems are often complex and contain numerous subsystems. If any of the subsystems fails, the whole software system could crash. This is a major risk and can be avoided by end-to-end testing. In our case, to test these functionalities script needs to go through the several other features: filtering/searching products, checking number of filtered products, previews, add product in cart...
* Integration - YES
	* As mentioned in end-to-end testing, features must work well separately and together. Interaction between different components should work as expected, and our tests confirm that perfectly.
* User Acceptance testing - NO
	* User acceptance testing comes at the end of testing chain, and its purpose is testing real-life, end user test scenarios before releasing it. I assume that this application is in production mode for a while, so this kind of testing should be performed before pushing the code on production.
