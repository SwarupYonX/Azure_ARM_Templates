Task 3: Deploy the ARM template
In the Azure Portal, open the Bash session within the Cloud Shell pane by clicking on the Cloud Shell icon.



Click on show advanced settings.



Enter a unique storage account name and a file share name, then click on Create storage button.



In the toolbar of Cloud Shell pane, select the Upload/Download files icon, select Upload From the dropdown and upload template.json file into the Cloud Shell home directory.



Now deploy the resources using the given command. This step may take a few minutes in order for the resources to get deployed successfuly.

az deployment group create --name <deployment-name> --template-file <path-to-template-file> --parameters adminUsername=<admin-username> adminPassword=<admin-password> --resource-group <resource-group-name>
NOTE: Copy this command to a text editor and replace:

‘<deployment-name>’ with the name of your deployment
`<resource-group-name>` with the name of your resource group which you can get from whizlabs page of the current lab session
`<path-to-template-file>` with the path to file containing the ARM template which in this case would be the file name
`<admin-username>` with the username
`<admin-password>` with the password of length greater than or equal to 12.


Task 4: Verify your deployments
After the successful execution of the above command, you will get a similar output on the CLI.



Go to your resource group in Azure portal to check your deployments.



Now, from the resources, you can see the Windows VM created.


