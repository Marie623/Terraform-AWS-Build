# Terraform-AWS-Build
This project was created from a guideline from FreeCodeCamp. The aim of this project is to create create a vpc, a subnet within the vpc, internet gateway, route tables and assign the subnet with the route table, and deploy it to AWS.

The first thing I had to do was to log onto AWS and create IAM user and then create a security key under "security credentials" of the IAM user that was previously created. The key file was downloaded and saved in a folder and the access code and key were made note of. Make sure you download the key file before you hit close. The purpose of the key pair is to allow connection to AWS when the resources are deployed.

I utilized Visual Code as a text editor and downloaded AWS and then added the key that was created by going to view => command pallet => AWS Create Credentials Profile. Doing this allow me to connect to AWS without adding my credential in my code and keeping it secure. 

In terraform use:

provider "aws" {
  region = "us-east-1"
  shared_credentials_files = ["~/.aws/credentials"]
  profile                  = "profilename"
  
 where "profilename" is the IAM user that was previously created". Now you are ready to code.

The ran into problems with deploying the code to AWS. The resources that I created were not showing when I went on Amazon AWS. I checked my code multiple times and everything as correct. You might find yourself asking, "What was the problem?"  I did not hit save. I initially hit save halfway through my code but did not save it again when I was finished. Lesson learned. Remember to always save whenever you make any changes or select auto save.

Have fun!

