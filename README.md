# az_aks_terraform_swgy
Creating Azure Kubernetes cluster svc &amp; deploying Swiggy clone app
Important Points 
Video -- https://youtu.be/UxOBAJlgzKM
===============================================================================================================================================================================================================================
A] Prerequisites
https://learn.microsoft.com/en-us/cli/azure/install-azure-cli-windows?tabs=azure-cli
https://code.visualstudio.com/download
https://learn.microsoft.com/en-us/azure/developer/terraform/configure-vs-code-extension-for-terraform?tabs=azure-cli
https://developer.hashicorp.com/terraform/install
https://kubernetes.io/releases/download/ 

===========================================================================================================================
D:\az_aks_terraform>terraform init

Initializing the backend...
+++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++
Initializing provider plugins...
- Finding hashicorp/random versions matching "~> 3.0"...
- Finding hashicorp/time versions matching "0.9.1"...
- Finding azure/azapi versions matching "~> 1.5"...
- Finding hashicorp/azurerm versions matching "~> 3.0"...
- Installing azure/azapi v1.12.1...
- Installed azure/azapi v1.12.1 (signed by a HashiCorp partner, key ID 6F0B91BDE98478CF)
- Installing hashicorp/azurerm v3.94.0...
- Installed hashicorp/azurerm v3.94.0 (signed by HashiCorp)
- Installing hashicorp/random v3.6.0...
- Installed hashicorp/random v3.6.0 (signed by HashiCorp)
- Installing hashicorp/time v0.9.1...
- Installed hashicorp/time v0.9.1 (signed by HashiCorp)

Partner and community providers are signed by their developers.
If you'd like to know more about provider signing, you can read about it here:
https://www.terraform.io/docs/cli/plugins/signing.html

Terraform has created a lock file .terraform.lock.hcl to record the provider
selections it made above. Include this file in your version control repository
so that Terraform can guarantee to make the same selections by default when
you run "terraform init" in the future.

Terraform has been successfully initialized!

You may now begin working with Terraform. Try running "terraform plan" to see
any changes that are required for your infrastructure. All Terraform commands
should now work.

If you ever set or change modules or backend configuration for Terraform,
rerun this command to reinitialize your working directory. If you forget, other
commands will detect it and remind you to do so if necessary.

D:\az_aks_terraform>terraform fmt

D:\az_aks_terraform>terraform validate
Success! The configuration is valid.

Outputs:

client_certificate = <sensitive>
client_key = <sensitive>
cluster_ca_certificate = <sensitive>
cluster_password = <sensitive>
cluster_username = <sensitive>
host = <sensitive>
key_data = "ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQClvCGYVSkfou8tCF0xBOI3+Ly2eb6x5h8qMVQ5DaLkYEkzGCY+GbcuypahbcTBYMIdATvvNDj4YTNWl+V37TH9RelhvdkXOKvNwCVoGAITBiHu2WNQeV3e/6tYlYbca1dPxUJVmgtaAQkM0tGI8Ui5sr2nA3RL4CYS1K8Bar22aTU99yXpSLx2eIK0c7EEmHP5pEPSQ8HytEcGI9+9Brj3B75oMAB41Ue42WVYTs40TrGV33QRRtEN1Dr52rjwbax7gmJ4XYjCOfIc4jMO82F2OofzAhVhD21P9B+yqzubdlXmSasZ/y8GloU5XOZhvtTD7E40Z5gq+FFThu7JKPf0MXtIoDvqxtg1GWEus10N5Lj89sap1LIy98BjZoHUldiZDHFly4sPkxxrqkZ8Y4CYaFLRd6d/q6bsFcl9Z13DQQosCjqD+AyP4rP4Ak0X6RBwJkF2oLIkUuj2ADsCfAgU1UiJZIdfhrgIJeLgjORlQ+U6kNi98H/PFaNOZTrk820= generated-by-azure"
kube_config = <sensitive>
kubernetes_cluster_name = "cluster-splendid-herring"
resource_group_name = "rg-helping-hors

Getting AKS Command Line Access from Visual studio code 
1.Kubernetes Extension should be installed in VS code 
![image](https://github.com/gautam4921/az_aks_terraform_swgy/assets/45917285/e1c4bab2-4cd5-44c9-8d58-41b8297c5bf2)

2. D:\az_aks_terraform>az account set --subscription 90f4dd64-b8a4-40a8-898f-a777acc25b9a

D:\az_aks_terraform>az aks get-credentials --resource-group rg-helping-horse --name cluster-splendid-herring --overwrite-existing
The behavior of this command has been altered by the following extension: aks-preview
Merged "cluster-splendid-herring" as current context in C:\Users\gautam.prasad\.kube\config
After that you can run each and every Kubectl command from vs code 


