## Google Chronicle Alerts Creator Job
This job will sync new SOAR alerts with Chronicle SIEM.
Note: This job is only supported from Chronicle SOAR version 6.2.30 and higher.


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://staging-chronicle.sandbox.googleapis.com/v1alpha/projects/spsstg-tsjkk/locations/global/instances/397fdff2-4666-4fa9-bab9-9ca374e6ab88|
|Verify SSL|Boolean|False|true|
|User's Service Account|Password|False|*****|
|Workload Identity Email|Password|False|*****|

## Google Chronicle Sync Job
This job will synchronize information about Chronicle SOAR Cases and Chronicle SOAR Alerts with Chronicle SIEM.
 Note: This job is only supported from Chronicle SOAR version 6.1.44 and higher.


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment|String|True|Default Environment|
|API Root|String|True|https://staging-chronicle.sandbox.googleapis.com/v1alpha/projects/spsstg-tsjkk/locations/global/instances/397fdff2-4666-4fa9-bab9-9ca374e6ab88|
|Max Hours Backwards|String|False|24|
|Verify SSL|Boolean|False|true|
|User's Service Account|Password|False|*****|
|Workload Identity Email|Password|False|*****|

## Simple Job Example
This is an example of a simple job. It has 2 functions: if a case has a tag "Closed", it will close the case from the job, if a case has a tag "Currency", it will add a comment to the case.


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|API Root|String|True|https://api.vatcomply.com|
|Verify SSL|Boolean|False|true|
|Password Field|Password|False|*****|


Adding a readme on ## Sync Incidents
This job synchronizes Google SecOps Alerts and Microsoft Sentinel Incidents. It ensures that comments, status, and tags are kept in sync between the two systems. For the job to identify the correct information, the Google SecOps case must have the “Microsoft Sentinel Incident” tag. If the alert didn’t originate from “Microsoft Azure Sentinel Incident Connector v2”,  you will need to add an “Incident_ID” context value to the case for the job to be able to find the correct information.


**Run Interval In Seconds:** 60

#### Parameters
|Name|Type|Is Mandatory|Value|
|----|----|------------|-----|
|Environment Name|String|True|Default Environment|
|Azure Active Directory ID|String|True|dsadsadsdsadsadsd|
|OAUTH2 Login Endpoint Url|String|True|https://login.microsoftonline.com|
|API Root|String|True|https://graph.microsoft.com|
|Client ID|String|True|dfdsfdsfdfdsfdsffd|
|Client Secret|Password|True|*****|
|Max Hours Backwards|Integer|False|24|
|Verify SSL|Boolean|False|true|


Adding a readme on 