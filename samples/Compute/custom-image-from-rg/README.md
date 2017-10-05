# Allow only a custom VM image

This policy will ensure that only a custom image from a Resource Group is allowed.

## Deploy Policy to Azure

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/?feature.customportal=false&microsoft_azure_policy=true#blade/Microsoft_Azure_Policy/CreatePolicyDefinitionBlade)

## How to create Policy Definition using PowerShell

````powershell
$definition = New-AzureRmPolicyDefinition -Name allowCustomImage -Policy 'https://raw.githubusercontent.com/Azure/azure-policy-samples/master/samples/Compute/custom-image-from-rg/azurepolicy.rules.json' -Parameter 'https://raw.githubusercontent.com/Azure/azure-policy-samples/master/samples/Compute/custom-image-from-rg/azurepolicy.parameters.json'
````

## How to create Policy Definitions using AzureCLI

````cli

Az policy definition create –name allowCustomImage -rules 'https://raw.githubusercontent.com/Azure/azure-policy-samples/master/samples/Compute/custom-image-from-rg/azurepolicy.rules.json' –params 'https://raw.githubusercontent.com/Azure/azure-policy-samples/master/samples/Compute/custom-image-from-rg/azurepolicy.parameters.json'

````