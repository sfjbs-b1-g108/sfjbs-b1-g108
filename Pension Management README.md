                                              **PENSION MANAGEMENT**
TEAM MEMBERS

KAVYA KATIKALA.
BHARGAV GUDIPADU.
SRAVANTHI CHIGURU.
PAMIREDDY CHANDRA SEKHAR REDDY.

ABSTRACT
Give the discouraging record of the traditional pension system and the limited coverage of the private and public sector pension scheme , there is need for robust web-based pension fund management system that can handle the pension process efficiently . This work focus on the design and implementation of a web-based pension fund management application to replace the manual system thus getting rid of the hurdles involved in the traditional pension management process.

INTRODUCTION

         Pension is an arrangement of providing peoples with an income when they are no longer earning a regular income from employment .However, pension should not be confused with severance pay, The terms 'retirement plan ' or 'superannuation, refers to a pension granted upon retirement. Retirement plans may be set up by employers, insurance companies, the government or other institution such as employer association or trade union.
       The manual method of pension fund management maintains or keep record in a filing cabinet about each employee/pensioner that is registered with a Pension Fund Administrator (PFA). When an employee decides to open an account with a PFA for the purpose of retirement savings, the former(pensioner) has to go the phusical location to obtain and fill a register form.
       
PROJECT_POINTERS

* Create at least 2 microservices
* Have their project up and synced on github
* we need to create Readme files
* should have used Netflix OSS libraries : Eureka, Hysterix, ZuulProxy
* should have create docker images of their Microservies
* should have used kafka
* All points should be working as per requirements
* should have the project presentation ppt ready on the project demonstration day by day

REQUIREMENTS
* Provides information about the registered pensioner detail i.e., Pensioner name, PAN, bank name, bank account number, bank type – private or public
* Determines if it’s a self or family pension. Calculate the pension amount and bank service charge post data authentication, and display on the web application user     interface
* This module should receive input from the web application
* A Web Portal that allows a member to Login and allows 
  to do following operations:
* Login
* Load the pensioner detail through the Pensioner detail module
* Post validation of the pensioner detail, pension amount should be displayed on the UI. This happens on invocation of ProcessPension module
* Store the pensioner detail, pension amount and the bank transaction detail in database

HARDWARE AND SOFTWARE REQUIREMENTS FOR PROJECT
1. Hardware Requirement:
a. Developer Desktop PC with 8GB RAM
2. Software Requirement (Java)
a. Spring Tool Suite (STS) Or any Latest Eclipse
b. Have PMD Plugin, EclEmma Code Coverage Plugin 
c. Configure Maven in Eclipse
d. Maven
e. Docker (Optional)
f. Postman Client in Chrome
g. git


##System Requirements
 Functional Requirements – Process PensionMicroservice
 
*Functional Requirements
Process Pension Microserviceshould be invoked from the web application. It allows the following 
*operations:
• It takes in Aadhaar number and determines the Pension amount and bank service charge
• Verifiesif the pensioner detail is accurate by getting the data from
PensionerDetailMicroservice or not. If not, validation message “Invalid pensioner detail 
provided, please provide valid detail.”. If valid, then pension calculation is done and the 
pension detail is returned to the Web application to be displayed on the UI

*Entity 
*ProcessPensionInput
1. Aadhaar number
*PensionDetail
1. PensionAmount
2. BankServiceCharge
REST End Points 
ClaimsMicroservice
POST:/ProcessPension(Input: processPensionInput| Output: PensionDetail)
Trigger – Should be invoked from Pension management portal
