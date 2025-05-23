# **Databricks_ETE**
Databricks End to End Project 

Project Outlook 

![alt text](<Screenshots/Screenshot 2025-05-22 204639.png>)

Let's Go Step by Step 

1. Create your Azure Resource Group 
2. Create your ADLS Gen 2 (bronze,silver, gold & metastore)
3. Create your Databricks 
4. Create your Databricks Connector and under ADLS IAM assign role assignment as Storage Blob Data Contributor -> Managed Identity -> Select Databricks Connector
5. Create Unity Catalog in https://accounts.azuredatabricks.net/ 
    Catalog -> Create Metastore -> location adls metastore  
    ***Note: You can only create one metastore for a region .***

    Under Access Connector ID : Databricks Connector -> Resource Id 

    Assign it to workspace 

Now Create catalog in Databricks Workspace 
    Then under External Data -> Credentials -> Create Credentials -> Under access connector id -> Use databricks connector Resource ID -> Create    

Creating External Location for Source, Bronze, Silver and Gold containers
     External Data -> External Location -> Connect each container in url and use storage credentials created before  

So Successfully Connected to Databricks to containers 

Now lets Create Schema using UI under Catalog -> Create Schema -> bronze

Also we can create table using Data Ingestion connector 

So this is overall set up and I have attached my notebooks for further reference 