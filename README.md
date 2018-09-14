# AWSBACKUP
Create Lambda Backup Function
This function will allow us to backup every instance in our account under the region we put the lambda function, that has a “Backup” or “backup” key tag
This script will search for all instances having a tag with “Backup” or “backup” on it. As soon as we have the instances list, we need to get all the EBS volumes on each instance in order to have the list of EBSs to be backed up. Also, it will look for a “Retention” tag key which will be used as a retention policy number in days. If there is no tag with that name, it will use a 7 days default value for each EBS instance.
steps to create the function:
•	Go to Services, Lambda, and click Create a Lambda Function
•	Skip the blueprint screen
•	Write a name for it (ebs-backup-worker)
•	Select Python 2.7 as a Runtime option
•	Paste the code below
•	Select the previously created IAM role (ebs-lambda-worker)
•	Click Next and Create Function

