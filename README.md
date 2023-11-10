<strong>Selenium Automation Framework</strong>

**--------------------------------------------------**

__Overview__

**--------------------------------------------------**

This is a Selenium-based automation framework for web application testing. It is designed to facilitate the creation and execution of automated test cases using JSON files.



**Features**

**--------------------------------------------------**

•	Converts Selenium IDE JSON test scripts to a format compatible with the framework.

•	Supports various types of test steps: type, click, select, output.

•	Allows dynamic modification of key-value pairs in JSON files.

•	Handles assertions using pattern matching.

•	Easy configuration using a properties file.



<Strong>Getting Started</Strong>

**--------------------------------------------------**

**Prerequisites**

Java Development Kit (JDK)

Maven

ChromeDriver (or WebDriver for your preferred browser)

**Setup**

Clone this repository to your local machine as a Existing maven Project

**Usage**

> * Place your Selenium IDE JSON test scripts (.side files) in the SideFile folder under **(src/test/resources/SideFile)**

> * Run the testRunner as **JUnitTest** to convert and execute the test cases

> * **Naming Convention** - The converted JSON files are given filenames that match the original .side file names, maintaining a clear association between the two.

> * The converted test scripts will be executed using Selenium WebDriver, and the results will be displayed in the console.

> * Modified, Framework Understandable Formatted  JSON File will be stored in the **Transformedinput** folder. **(src/test/resources/ Transformedinput)**


**Configuration**

**--------------------------------------------------**

**config.properties:** Configure properties and specify whether to perform regression testing.

**FileToTransform:** Specify which .side files to transform (All or specify a file name or No)

>•	All -  This option will process all the .side files found in the specified folder and convert them to the framework's understandable JSON format. It will automatically identify and process all the files within the designated directory.

>•	No -  When this option is selected, the framework will not perform any actions related to the transformation. It's equivalent to a "no-action" mode and will effectively skip the conversion process. This can be useful when you want to temporarily disable the conversion functionality without removing or commenting out configurations.

>•	Specify Single or Multiple File Name : You can specify one or more specific .side file names that you want to convert. If you have multiple files to specify, separate their names with commas (,). The framework will only process the files you explicitly specify using this option.

For example:

* To convert a single file named test1.side, set **FileToTransform =test1**

* To convert multiple files, such as test1.side, test2.side, and test3.side, set **FileToTransform = test1,test2,test3**

**Regression:**  Specify which .json files to Run Regression (All or specify a file name or No)

>•	All: When you set Regression = All, the framework will execute regression testing for all available .json files in the specified folder. It will run the Selenium automation tests as per the comments and instructions provided in each .json file. This option is useful when you want to automate and perform regression testing for all test cases in your project.

>•	No: If you set Regression = No, the framework will not perform any actions related to regression testing. This effectively disables the regression testing functionality, allowing you to skip running regression tests temporarily. This can be handy when you want to focus on other testing tasks or need to troubleshoot without executing regression tests.

>•	Specify Single or Multiple File Name: You can specify one or more specific .json file names that you want to use for regression testing. Separate the file names with commas (,). The framework will only execute the regression tests for the specified files. This option gives you granular control over which test cases to include in regression testing.

For example:

* To run regression testing for a single file named test1.json, set **Regression = test1**

* To run regression testing for multiple files, such as test1.json, test2.json, and test3.json, set **Regression = test1,test2,test3**

**SideFilePath:** Path to the folder containing .side files **(src/test/resources/SideFile)**

**JSONInputFolder:** Path to the folder where modified JSON files will be stored **(src/test/resources/Transformedinput)**
 

**Folder Structure**

**--------------------------------------------------**

* **src/test/java** : Java & Selenium source code for the framework.

* **src/test/resources** : Configuration files and test data.
•	SideFile : Place your Selenium IDE JSON test scripts here.
•	Transformedinput : Modified test scripts and test results.



**Contributing**

**--------------------------------------------------**

Contributions are welcome! Feel free to open issues, provide feedback



**Acknowledgments**

**--------------------------------------------------**
* Selenium - Web automation framework.

* JSON - Data interchange format.
