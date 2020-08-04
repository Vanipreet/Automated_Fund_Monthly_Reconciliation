# Fund_Monthly_Reconciliation

# Table of Content
### [Introduction](#introduction-1)
### [Assumptions](#assumptions-1)
### [Automated_Fund_Monthly_Reconciliation_processflow diagram](#automated_fund_monthly_reconciliation_processflow-diagram-1)
### [Steps to run the macro](#steps-to-run-the-macro-1)
  #### [Happy day scenario](#happy-day-scenario-1)
  #### [Exceptional condition: Some transactions available on either of the two which is not available on the other sheet](#exceptional-condition-some-transactions-available-on-either-of-the-two-which-is-not-available-on-the-other-sheet-1)
### [Forward](#forward-1)

# Introduction
The purpose of [Fund_Monthly_Reconciliation_Macro.xlsm](https://github.com/Vanipreet/Automated_Fund_Monthly_Reconciliation/blob/master/Fund_Monthly_Reconciliation/Fund_Monthly_Reconciliation_Macro.xlsm) is to create an automated process for the execution of Portfolio's / Fund's Monthly Reconciliation. There are multiple assumptions and pre-requisites that has been kept in place for the smooth execution of this macro.

# Assumptions
This macro is built with few assumptions in mind as listed below

1. For the macro to run, we need two external data inputs, Monthly Bank_statement and Monthly Broker_statement
2. The macro is prepared for the purpose of Monthly Reconciliation and hence uses monthly reconciliation files
3. Macro and the data inputs are available under "H:\Fund_Monthly_Reconciliation" directory, however as per the drive parition, this can be amended
5. Macro expects static input data. However with appropriate mapping, database can be also accurately utilized


# Automated_Fund_Monthly_Reconciliation_processflow diagram
![alt text](https://github.com/Vanipreet/Automated_Fund_Monthly_Reconciliation/blob/master/Monthly%20Reconciliation%20Process.PNG)

# Steps to run the macro

1. Download the zip file [Fund_Monthly_Reconciliation](https://github.com/Vanipreet/Automated_Fund_Monthly_Reconciliation/tree/master/Fund_Monthly_Reconciliation) onto your preferred location and unzip the file there
2. Open Fund_Monthly_Reconciliation_Macro.xlsm workbook
3. Right click on macro button "Monthly Reconciliation"
4. From the drop down options click on "Assign Macro"
5. Select "Monthly_Recon" and click on "Edit" button
6. Under module 1, map the broker statement, bank statement, Monthly Reconciliation file directory as per requirement
Please Note: All the mapping is required only on the Module 1
7. For test run, change the file name "Bank_Statement_08-2020" to current Month, Year. Save the file and close
8. Redo the Step 7 for "Broker_Statement_08-2020" as well. Save the file and close
9. Click on "Monthly Reconciliation" macro button
### Happy day scenario
10. When macro has completed processing, summary sheet will be visible on the screen. Go through the summary sheet
11. Close the "Monthly_Reconciliation - MM-YYYY.xlsx" sheet

### Exceptional condition: Some transactions available on either of the two which is not available on the other sheet
11. Add few new transactions in either the Bank statmenet or broker statement sheets ()
12. Go through the summary sheet for this new recon sheet

# Forward

This macro is a starting step for Monthly Reconciliation of fund/ portfolio, utilizing some tweaks this can accurately fulfil Monthly calculation requirement.

However the bigger picture is that instead of making this macro to work on a single fund, it can be accurately "Looped" for multiple funds.

This macro can be accurately mapped to incorporate Daily/ Weekly/ Quarterly and Annual reconciliations as well.

If this macro is to run on windows system, "Task Scheduler" can be utilized to automatically update the input files at a precribed time from the source drive and also to automatically run this macro so monthly reconciliation can be calculated without any human intervention. 
(Apple systems might also have something similar to task scheduler that can be utilized)

