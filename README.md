## ADO picklist fields list
This utility helps to extract the unique Azure DevOps fields that have picklist values, this can serve to prune fields that might no longer be used.
It gives the names of the readable fields only from another utility developed by Dan Hellem that outputs guid and field names.

Have you ever faced the dreaded error:
VS402846: The number of picklists in the collection has reached the limit of 2048.?

![image](https://github.com/renaudmontesMSFT/ADO-picklistfields-list/assets/100614151/5bbd4748-6adb-420d-8271-e4ffc7f7cea2)

Chances are ff you work in an organization with many projects or fields, you might eventually face this problem, but where to start?
Don't despair, follow these easy steps:
# Step 1
Clone Dan's GitHub repo and compile the code to get the utility exe file, this will produce the input for this notebook
https://github.com/danhellem/azure-devops-admin-cli 

adoadmin.exe /org:{myorg} /pat:mypat /action:allpicklists >rawoutput.txt
Notes:
1- Create a new PAT (Personal Access Token) in ADO
2- The > in the command prompt indicates to produce a file rather than display results on the screen

# Step 2:
Run this notebook!
Input: rawoutput.txt 
Output: Unique fields in ADO to review which fields with picklist values might be prime for pruning, file name will be called: picklist_fields.csv

# Step 3:
Go to your ADO organization's settings and start removing those fields that might be no longer needed





