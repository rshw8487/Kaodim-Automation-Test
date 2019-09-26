# Kaodim-Automation-Test

# Kaodim Automated API Test Suite

https://www.getpostman.com/collections/f053c3078f93ffac182d

Steps to execute:

Runner-> Select enviornment e.g QA Envionrnment and no of iteration click on run.

Guide me if you expected something else so I Will update test suite accordingly.

# System Architecture & Design

Solution
Designed and built a solution to automate mobile testing for the client based on the open-source tool Selenium Appium. The solution also used the Amazon Web Services (AWS) Device Farm to eliminate dependencies on device and network availability. 

Benefits 
The solution proved to very beneficial in reducing hours of manual test effort, including: 
• Decreasing overall regression cycle time by 40% 
• Decreasing overall testing cost by 30% 

Additionally, we’ve achieved:
 • Increased regression test coverage by 30%
 • Creation of low-maintenance test scripts

Automation Strategy
Purpose to create test strategy using automation to effectively shorten the regression cycle. The key to success was the selection of the right tool and implementation. We selected an open-source tool, due to the obvious benefit of no license fees. Additional benefits include:
• The framework can be expanded for any customization 

• An active community exists which helps to resolve any issues 

• Frequent updates are made to the tool

Features Considered for Tool Selection
There are many tools available (both open source and commercial) for automating mobile application testing. Choice of automation tools or frameworks is vital for the success of an automation strategy. As an aid in tool selection, we listed key features that the automation tool would need to have in order to automate application testing for this client.
 

Tools used:-
Appium Studio (Android and iOS)

MonkeyTalk (Android and iOS)

Putting Together an Automated, Mobile App Testing Solution
The following components were used to implement an integrated, mobile app testing solution.
 

 
Challenges Encountered

1. Initial setup of Appium can be time consuming. 

2. During initial execution, upload of test to the AWS Device Farm scripts was taking a long time, but after we contacted AWS support, they resolved the problem. 

3. On iOS we can only run one instance on Instruments per Mac OS, so we can only run Appium scripts on one device per Mac machine. If we want to run our tests on multiple iOS devices at the same time, then we would need to arrange for the same number of Mac machines, which would be a costly affair. This limitation was resolved by executing our scripts in the AWS Device Farm.


In my previous project, I used OneFramework :-
If you've application in android, ios & web platforms and want to automate with single code base then this framework is good choice.
This is a generic Page Object Model which solves all your automation needs with single codebase.
We often tend to create different test frameworks for different platforms and it's very difficult for anyone to serve all platform needs in one test automation framework.
OneFramework solves all your needs. You just give the locator and leave the rest to OneFramework.

Contents:
•	Features

•	Libraries Used

•	Prerequisites Installations

•	Appium Setup

•	How This Framework Works

•	How To Run Tests

•	How To See Allure Result Report

Features:
•	Easy to automate any type of application
•	Cross platform(mobile & web) support with single codebase
•	Page Object Model
•	TestNG integration
•	Image Comparison
•	Allure Reporting
•	Robust in nature
•	Many configurations

Libraries Used:
1.	Appium
2.	Selenium WebDriver
3.	Java
4.	TestNG
5.	Gradle
6.	WebDriverManager
7.	Allure Report

Prerequisites Installations:

1.	JAVA 1.8 - Install Java and set the JAVA_HOME path on your machine.

2.	Node & NPM - Download & install node from https://nodejs.org/en/download/.

3.	Gradle - Install Gradle.

4.	Android - Install Android Studio & set ANDROID_HOME path.

o	Downloading the Android SDK

o	Download the Android SDK tools such as

a.	Build tools

b.	Platform tools

c.	Android Emulator

d.	Intel HAXM installer etc.....

e.	Create an emulator device from AVD manager

5.	iOS - Install XCode on your machine & download required iPhone/iPad simulators.

6.	Allure Report - Install Allure Report library on your machine. Please follow below link to install it on MAC.

Similarly install allure-report installer on your respective machine.https://docs.qameta.io/allure/#_installing_a_commandline
Note: If you want to run only on WEB, you don't need anything except JAVA.
Mentioned installations Node, Android & iOS are for mobile app automation & Rest like Gradle & Allure are for framework level

Appium Setup:

•	Install Appium
 $ sudo npm install -g appium@1.9.1 --unsafe-perm=true --allow-root 
 
•	Appium Doctor - which is used to see if the appium setup is correctly done or not. Run it and fix the issues as per that.
 $ sudo npm install -g appium-doctor --unsafe-perm=true --allow-root
 $ appium-doctor

How This Framework Works:

This framework is built in Page Object Model style using TestNG framework.
We have "testng.xml" file which has tests for each and every platform in cross browser/device testing fashion.
Here are the minimal things you have to do:

•	Create your tests

•	Create your Page Object class w.r.t test that you have written, if not created already (Take the reference from org.oneframework.pageObjects).
For e.g, SignIn button locators for web, ios & android set as shown below.
 
- If mobile app, Set the android, ios device details in corresponding files in resources directory as shown below

- If web app, Set web app URL in BaseTest

How To Run Tests:

1.	Clone the repo.

https://github.com

2.	Build the JAR and run it.

$ gradle clean build
$ java -jar build/libs/Automation-1.0-SNAPSHOT.jar capture
$ java -jar build/libs/Automation-1.0-SNAPSHOT.jar compare

Note:capture & compare are the image capture and compare modes.

How To See Allure Result Report:
Once test execution is complete, allure-results directory gets generated. I assume you have already installed allure on your machine. If not, install it. If yes, run below command to see the report.

$ allure serve <allure-results path>

    

