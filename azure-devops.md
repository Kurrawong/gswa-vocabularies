# Azure DevOps setup notes

## Create the variable group

1. Open Azure DevOps and go to Pipelines -> Library.
2. Select + Variable group.
3. Name it `vocabs-dev`.
4. Add a variable named `SERVICE_BUS_CONNECTION_STRING`.
5. Mark it as secret.
6. Under pipeline permissions, enable "Allow access to all pipelines" (or authorise the pipeline when prompted). The pipeline needs to be created before this step can be completed.

## Populate the Service Bus connection string

1. Open the `vocabs-dev` variable group.
2. Paste the Service Bus connection string into `SERVICE_BUS_CONNECTION_STRING`. Mark it as secret.
3. Save the variable group.

## Wire pipeline to GitHub repository

Create a new pipeline in Azure DevOps and connect it to the GitHub Repository. Use the existing `azure-pipelines.yml` file in the repository to configure the pipeline.