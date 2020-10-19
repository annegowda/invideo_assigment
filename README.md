# invideo_assigment
# Project Name: Cucumber_Framework

Cucumber + Selenium + Maven based automation framework solution

## Pre-requisites
1. Eclipse IDE (Photon or later)
2. JDK 8+

## Installation

1. Unzip the file to a particular location
2. Import as a Maven project into Eclipse IDE

## Usage

1. In Eclipse IDE, Right-click project and select: Run as -> Maven test
OR
2.Open comment promt ,navigate to project folder :mvn test
OR
3. Right-Click TestRunner class (inside runners package in src/test/java folder)
	and select - > Run as JUnit Test

## Configuration

1. Configuration is defined in Config.properties (in project root folder)
2. Use the following values as required (All lowercase):
	browser = firefox 
	or 
	browser=chrome 
	
	implicitlyWait=<integer> value in seconds
	url=<url to test>
3. geckodriver and chromedriver paths are relative to the priject.
	Do NOT modify if not required.

## Project Structure

1. src/main/java has classes for the cucumber framework.
2. src/test/java has Testrunner and test Step Definitions
3. src/test/resources has Cucumber feature files and webdriver executables
4. ./reports/      has json and html reports


## Package/Class Information

1. src/main/java/core/BrowserFactory - handles webdriver path config and launching the requisite Browser instance
2. src/main/java/core/ConfigReader - reads configuration properties from the Config.properties file in project root folder
3. src/main/java/core/PageObjectManager - Helper class abstracts Page Object creation
4. src/main/java/core/TestContext - Abstracts the core object access for tests
 src/main/java/utility/ApplicationspecificMethods - class have ApplicationSpecific methods like handle frame
5. src/main/java/enums/BrowserTypes - enumeration of Browser Types supported by framework
6. src/main/java/webpages/BankOTPPage - Page class with methods for Bank OTP page
7. src/main/java/webpages/CartPage - Page class with methods for Shopping Cart page
8. src/main/java/webpages/HomePage - Page class with methods for Application Home page
9. src/main/java/webpages/OrderSummaryPage - Page class with methods for Reviewing Order summary before purchase
10. src/main/java/webpages/PaymentPage - Page class with methods for Payment page
11. src/main/java/webpages/ - Page class with methods for Shopping Cart page
12. src/test/java/runners/TestRunner - Entry point for execution with cucumber tests configuration via CucumberOptions annotation
13. src/test/java/stepDefinitions - Java Test steps matching the steps defined in the cucunmber feature files
 src/test/java/stepDefinitions/Hooks - Java class help us to setup driver and tear down driver.
14. src/test/resources/functionalTests - folder containing cucumber tests written in Gherkin language, configured via CucumberOptions->features property in TestRunner class
15. src/test/resources/webdriver - folder containing webdriver executables, configured via Config.properties file

## Credits

Written by: AnneGowda
