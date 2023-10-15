# Software User Manual

## *Usage*

MT4WS serves several key purposes in software testing and quality assurance:

***Automated*** ***Testing***: uMT is designed to automate the testing process, reducing the manual workload. It is used for the automated discovery and execution of test cases to verify software correctness.

***Metamorphic Relations Discovery and Verification***: A core objective of uMT is to aid users in discovering and verifying Metamorphic Relations, critical test specifications for software validation. Through uMT, users can effectively identify these relations, thus enhancing their software testing.

***Enhancing Test Coverage***: uMT assists in improving test coverage, ensuring comprehensive testing of various aspects of software to uncover potential defects.

***Quality Assurance Support***: uMT contributes to the enhancement of software quality by automating testing and MR validation, reducing the risk of errors and defects.

*tool website*：http://www.mt4ws.cc/

## *User Guide*

The MT4WS tool is presented to users through a JSP web page for human-computer interaction. Interaction with users during testing is done in a "wizard" style. The "wizard" method presents users with limited information at each step, along with detailed usage instructions. The advantage of this method is that it makes it easier for users to get started and facilitates ease of operation.

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps12.jpg) 

<center> Figure 1: MT4WS System Welcome Page</center>

### 1.Welcome Page

When users enter the welcome page as shown in Figure 1, they are presented with a WSDL URI input box. Users should enter the WSDL address of the web service they wish to test into this box and click the "start" button to parse the WSDL entered in the text box. If the parsing is successful, the process proceeds to the "Select Interface to Test" step. In case of failure, an exception is reported. Alternatively, users can choose to upload WSDL files.

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps13.jpg) 

<center> Figure 2: Operation Selection Page</center>

### 2.Select Operation Page

Clicking the "start" button takes you to the WSDL operation list page, as shown in Figure 2. This page displays a list of all the operations included in the web service to be tested. These are presented in the form of radio button groups. Users can choose a specific operation to test by clicking the radio button corresponding to that operation. When a particular operation is selected, clicking the "next" button takes you to the "Input Metamorphic Relations" step, while clicking "back" returns to the welcome page.

### 3.Input Metamorphic Relations

Input one or more metamorphic relations on a specified operation interface, and the interface is shown in Figure 3. The tool currently supports two modes for defining metamorphic relations, manual interaction mode and batch (file import) mode. It also supports two methods for obtaining metamorphic relations: data mutation-based metamorphic relation acquisition and composite metamorphic relation generation.

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps14.jpg) 

<center> Figure 3: Metamorphic Relation Input Page</center>

When defining metamorphic relations manually, as shown in Figure 3, "Define Metamorphic Relations Manually," the user needs to manually input input and output relations for the metamorphic relation. In the input relationship, the user defines function expressions for the input vectors of the original test case in the "Source" column and for the input vectors of the follow-up test case in the "Follow-up" column. In the "Relation" column, an operator for binary relations is selected to describe the relationship between the original test case and the follow-up test case. Similarly, in the output relationship, the user defines function expressions for the output vectors of the original test case, output vectors of the follow-up test case, and binary relation operators. After inputting one set of R and Rf, the user clicks the "Add to MR set" button to store the data in the database. Users can click the "Check MR set" button at any time to view the saved metamorphic relations.

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps15.jpg) 

<center> Figure 4: View Metamorphic Relation Page</center>

To use composite metamorphic relations, two or more metamorphic relations need to be predefined, and metamorphic relations already input and stored, as shown in Figure 4. Click the "Compose" button to execute the composite method, create a new composite metamorphic relation, and store it for use in subsequent metamorphic testing.

To obtain metamorphic relations by importing a file, as shown in Figure 3 with "Import from XML file," the tool automatically reads the MRDL file and stores it. The specific format can be found in the "mrdl_transfer.xml" file.

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps16.jpg) 

<center> Figure 5: Data Mutation Page</center>

To define metamorphic relations using the data mutation-based method, as shown in Figure 5 with "Data Mutation," select data mutation operators, input variables, output variables, and binary relation operators. Click the "Add to DM set" button, and the system exports the corresponding metamorphic relations based on mapping rules and stores them. Click "Next" to enter the test case generation page.

### 4 Select Original Test Case Generation Method

 

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps17.jpg) 

<center> Figure 6: Original test case generation Page</center>

After entering the metamorphic relations, you'll reach the original test case generation selection page, as shown in Figure 6. This testing tool provides three methods for generating original test cases: manual input, automatic generation, and file import. If you select manual test case generation, you must first choose a metamorphic relation and then manually enter the values of each variable in the original test case in the corresponding text boxes. The test cases are then added to the database. If you choose to import test cases from a file, you provide a file containing data for several original test cases. The tool automatically imports test cases from the file, and the file format follows "ATMTestCaseSet.xml." If you select random automatic test case generation, a certain number of valid test cases are automatically generated using random value methods for all metamorphic relations. The quantity can be specified by the user. Click "Next" to enter the test configuration page.

### 5.View Test Information

The test configuration page, as shown in Figure 7, allows users to view information about the web service to be tested, the operations to be tested, original test cases, follow-up test cases, and input metamorphic relations. Users can also configure their own test information by clicking "configuration" to enter the configuration selection page.

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps18.jpg) 

<center> Figure 7: View Test Information Page</center>

### 6.Test Information Configuration

In this configuration page, as shown in Figure 8, users can select the metamorphic relations to be verified and several test cases from the selected metamorphic relation's test case set. Click "Submit" to save the test configuration, and return to the test information view page.

 

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps19.jpg) 

<center> Figure 8: Test Information Configuration Page</center>

### 7.Execute Test

The test execution process page, as shown in Figure 9, displays the service name and operation interface being tested.

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps20.jpg) 

<center> Figure 9: Execute Test Page</center>

### 8.View Test Report

![img](https://github.com/MuMT-USTB/mumt/blob/main/MT4WS%20User%20Manual.assets/wps21.jpg) 

<center> Figure10: View Test Report Page</center>

After completing the test, you will enter the view test report page, as shown in Figure 10. This page provides detailed information about the test results. The first section, from top to bottom, includes information about the web service being tested, including the web service name, WSDL URI, and the start and end times of the test. The second section provides overall statistical results, listing all the operations tested in this session, and it shows the names of all the operations in the web service, including the invalid and valid operations. Valid operations are highlighted in black font, and invalid operations are shown in red font. The third section provides detailed information about invalid operations. It lists which metamorphic relations the operation fails to satisfy and which test cases discovered errors for each unsatisfied metamorphic relation. If users wish to view detailed information about metamorphic relations or test cases, they can click the "Check MRs" and "Check Test Suite" buttons. Users can click "Download Test Log" to download the test log. Finally, click "Exit MT4WS" to exit the tool and close the page.

 