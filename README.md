# reporting-jobs-tekton-definitions

This tekton pipeline is used to initiate reports for CD-Broker and CD-Bss Apps and the pipeline is scheduled to run every 4 hours.

#### Cron expression implemented: 0 */4 * * *

## Pipeline-Level Environment Variables

### Username

Username is common for both apps and is passed in as a variable under **environment properties**

## Listener-Specific Environment Variables 

### Url

A unique url which is being used in the curl command is also added under **trigger properties** for each app

#### CD-Broker: https://cd-broker.us-south.devops.dev.cloud.ibm.com/report_usage

#### CD-Bss: https://continuous-delivery-bss.us-south.devops.dev.cloud.ibm.com/api/v1/poll


### Password

A unique password for each app is also passed in as a variable under **trigger properties**
