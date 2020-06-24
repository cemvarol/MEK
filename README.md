az group create --name ConRG --location eastus

az container create --resource-group ConRG --name cemocon --image index.docker.io/cemvarol/aci:mek --dns-name-label cvaz061904mek --ports 80

az container show --resource-group ConRG --name cemocon --query "{FQDN:ipAddress.fqdn,ProvisioningState:provisioningState}" --out table

