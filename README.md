# AKS Demo

Deploy an Azure Kubernetes Cluster using ARM-templates and GitHub Actions. Source for the ARM-template:
https://github.com/Azure/azure-quickstart-templates/tree/master/101-aks

1. Create Service Principal for AKS
az ad sp create-for-rbac --name GitHubActionsDeploy --role contributor --scopes /subscriptions/380d994a-e9b5-4648-ab8b-815e2ef18a2b/resourceGroups/AKSDemo-Rg --sdk-auth
2. Add secrets for the service principal to the GitHub Project (Settings->Secrets)
3. Commit and push a change will trigger the Action and deploy the template
