## Introduction

  This APEX app supports:
  
- File upload to OCI object storage,
- Fetch filenames in the specific OCI bucket in a report and the ability to download these,
-	Leverage the OCI Generative AI Services and generate output for the same.


## App Configuration

1. **How to import this app**
   
  Import the above .sql file into your workspace and install the application. A detailed process to do that can be found [here](https://docs.oracle.com/en/database/oracle/apex/22.2/htmdb/importing-export-files.html#GUID-D01CF7A6-A593-4ACD-A92C-C94CAC100D61)

3.	**How to create web credentials**

    To create web credentials in APEX:
  
      - Login to APEX Builder
  
      - Workspace Utilities > Web Credentials > Click 'Create > '
  
      - Enter a 'Name' and 'Static Identifier'
  
      - Select 'Authentication Type' = Oracle Cloud Infrastructure (OCI)
  
      - 'OCI User ID' = Enter the user value; this starts with ocid1.user
  
      - For 'OCI Private Key', complete the following steps:
     
         - Open the file downloaded when you clicked the 'Download Private Key' button while creating the OCI Service Account. The content should look similar to the text below
   	 
         - Delete the first line -----BEGIN PRIVATE KEY----- and the last line -----END PRIVATE KEY-----
     
         - Remove all line feeds so that the text is just one continuous string
  
         - Paste the string into the 'OCI Private Key' field
  
      - 'OCI Tenancy ID' = Enter the tenancy value; this starts with ocid1.tenancy
  
      - 'OCI Public Key Fingerprint' = Enter the fingerprint value; e.g. e0:3b:eb:d6:cc:c2:ae:5e:3f:b0:45:09:ac:d6:14:f5


4. **How to configure REST data sources** 

    - To create and configure a REST endpoint in APEX, refer the documenttation [here](https://oracle-livelabs.github.io/apex/ai-vision-lab/workshops/tenancy/index.html?lab=3-integrate-oci-vision#Task1:ConfigureOCIVisionRESTAPIasRESTDataSource)
    - To enable the above configured endpoint in a specific page, refer the documentation [here](https://blogs.oracle.com/apex/post/automate-invoice-handling-by-integrating-your-oracle-apex-app-with-oci-document-understanding)


## Code Configuration

To configure the functional and Oracle Cloud Infrastructure components of this app refer the Github repository published [here](https://github.com/divbatra/dbloganalyzer)
