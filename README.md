## Cloned Repository  
This repository has been cloned from one of the Azure Quick Start Templates available at https://github.com/Azure/azure-quickstart-templates/tree/master/quickstarts/microsoft.network/azurefirewall-premium



# Create Testing Environment for Firewall Premium (IDPS, TLS Inspection, Web Categories)

[![Deploy To Azure](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.network%2Fazurefirewall-premium%2Fazuredeploy.json)

[![Visualize](https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true)](http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2FAzure%2Fazure-quickstart-templates%2Fmaster%2Fquickstarts%2Fmicrosoft.network%2Fazurefirewall-premium%2Fazuredeploy.json)

This template deploys a complete testing environment for Azure Firewall Premium enabled with IDPS, TLS Inspection, URL Filtering and Web Categories:

![Specification](./images/spec.png)

- The template deploys a new Azure Firewall Premium and Firewall Policy with predefined settings to allow easy validation of its core capabilities (IDPS, TLS Inspection, URL Filtering and Web Categories)
- The template deploys all dependencies including Key Vault and a Managed Identity. In a production environment these resources may already be created and not needed in the same template.
- The template generates self signed Root CA and deploys it on the generated Key Vault
- The template generates a derived Intermediate CA and deploys it on a Windows testing machine (WorkerVM)
- A Bastion Host (BastionHost) is also deployed and can be used to connect to the Windows testing machine (WorkerVM)
- Firewall Policy is pre-configured with TLS inspection and IDPS enabled. You can test it via the following URLs
  - Go to https://www.azure.com and inspect the certificate in the browser.
  - Go to https://azure.microsoft.com/en-us/community/events which is denied using a URL deny rule.

Azure Firewall is a managed cloud-based network security service that protects your Azure Virtual Network resources. It is a fully stateful firewall as a service with built-in high availability and unrestricted cloud scalability. You can centrally create, enforce, and log application and network connectivity policies across subscriptions and virtual network. Azure Firewall uses a static public IP address for your virtual network resources allowing outside firewalls to identify traffic originating from your virtual network.

Learn more at https://docs.microsoft.com/en-us/azure/firewall.

# Testing  
Testing of the premium sku features deployed through this repo can be performed using the steps provided in the microsoft documentation  
https://docs.microsoft.com/en-us/azure/firewall/premium-deploy#test-the-firewall


