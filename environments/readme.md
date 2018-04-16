# Environments Folder

This is a temporary folder where to store parameters required by templates for a given environment.
This will replaced soon by a SecureParametersResource from a Secrets Vault

## Colors Environment
This a just a random name for environment used for testing templates.

Use different colors as environment names for development and testing.
Modify the Environment parameter in the json files in `environments/colors` and the stack names accordingly.

Eg. green, blue, red

**Hosted Zone**  
```
aws cloudformation create-stack --stack-name blue-infra-hosted-zone --parameters file:///$PWD/environments/colors/infrastructure/vpc-env-hosted-zone.json --template-body file:///$PWD/infrastructure/vpc-env-hosted-zone.yml
```

**Web App**  
```
aws cloudformation create-stack --stack-name blue-account-webapp --parameters file:///$PWD/environments/colors/services/webapp.json --template-body file:///$PWD/services/webapp/webapp.yml
```
