# Update Remote Desktop Sesson Collection to new template image

<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-update-rdsh-collection/PublicLastTestDate.svg" />&nbsp;
<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-update-rdsh-collection/PublicDeployment.svg" />&nbsp;

<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-update-rdsh-collection/FairfaxLastTestDate.svg" />&nbsp;
<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-update-rdsh-collection/FairfaxDeployment.svg" />&nbsp;

<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-update-rdsh-collection/BestPracticeResult.svg" />&nbsp;
<IMG SRC="https://azurequickstartsservice.blob.core.windows.net/badges/rds-update-rdsh-collection/CredScanResult.svg" />&nbsp;

This template updates RDSH servers in existing session host collection with new updated template image. The URI for the image is provided as a template parameter.

This template deploys the following resources:
+ `<rdshNumberOfInstances`> new virtual machines as RDSH servers

Template does the following:
+ creates new RDSH instances from given template image  and  adds them to collection;
+ puts old  RDSH servers in Drain mode to prevent new user connections;
+ notifies any logged on RD users that their sessions will be soon terminated due to collection maintenance;
+ logs off existing users from old RDSH instances after given timeout (`<userLogoffTimeoutInMinutes>` parameter).

Note: Template does **not** delete or deallocate old RDSH instances, so you may still incur compute charges. These virtual machine instances may need to be deleted manually.

Click the button below to deploy:

<a href="https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fmmarch%2Fazure-quickstart-templates%2Fmaster%2Frds-update-rdsh-collection%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/deploytoazure.svg?sanitize=true"/>
</a>
<a href="http://armviz.io/#/?load=https%3A%2F%2Fraw.githubusercontent.com%2Fmmarch%2Fazure-quickstart-templates%2Fmaster%2Frds-update-rdsh-collection%2Fazuredeploy.json" target="_blank">
    <img src="https://raw.githubusercontent.com/Azure/azure-quickstart-templates/master/1-CONTRIBUTION-GUIDE/images/visualizebutton.svg?sanitize=true"/>
</a>

