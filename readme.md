Precisions on values format to set : 
- searchDomain : private.***.com
- storageKey : Azure Storage Account Primary / Secondary Key (not the entire connection string)
- subnetId : The entire subnet resource id as follows "/subscriptions/___/resourceGroups/___/providers/Microsoft.Network/virtualNetworks/___/subnets/___"
- Azure_Credentials : Provided by az ad sp create-for-rbac --scope ... as explained in the [Azure/Login@v1](https://github.com/marketplace/actions/azure-login) Github Action

The example uses a [securestring replace action](https://github.com/jwsi/secret-parser) : Bear in mind it's not the recommended way as real Infra-as-Code should be done through trusted solutions (Terraform, Bicep, etc.) relying on secrets stored in an Azure Key Vault. 