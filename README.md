# Automate EC2 Instance Creation with GitHub Actions on Commit.
 
This is the basic guide of whenever Commit happens in the GitHub it should trigger GitHub actions and an EC2 Instance should be create. 


# create an IAM user and give necessary permissions (EC2 FullAccess) & generate keys.

First go to the IAM management console >>>> go to the users >>>> click on the create user >>>> specify all the details >>>> attach necessary policies (EC2 FullAccess) >>>> review and create an IAM user.
Then click on the IAM user you just created >>>> go to the security credentials >>>> scroll down & you can see create access key click on it >>>> choose the use case (Command Line Interface(CLI)) >>>> give desciption tag value (GitHub Keys) >>>> create access key >>>> store or download that access key  as csv file.


# Create a GitHub Repository & Add AWS Credentials in GitHub Environment secrets.

First go to your GitHub home page >>>> then on the left side you can see your profile photo click on that >>>> click on your repository >>>> click on new >>>> give suitable name and description that you want to give and check Add a readme file >>>> click on create repository.
Go to your repository secrets >>>> Click on settings >>>> On the left down side you can see secret and variables click on that >>>> click on actions >>>> Add your secrets.


# Create a workflow.yml file, main.tf, & provider.tf in visual studio code  & add given code in that.

First create a folder (.github) >>>> inside that folder create one more folder (workflows) >>>> inside that folder crate a file (create-ec2.yml).
Then create a file (main.tf & provider.tf) outside of .github folder >>>> And add given terraform code as it is.


# Push your files to GitHub repository & it will triggere automatically and an EC2 instance will be launch.

First Create a folder in your desktop or whatever place you want to >>>> Then go to that folder and right click and click on show more folder then click on open Gitbash here.
Then type some commands one by one >>>> git clone and your github repository link then press enter >>>> cd your folder name >>>> ls (it can show whatever in that folder) >>>> git add . >>>> git commit -m "pushpa" >>>> git push.

$$ Then your code will push on the repository and it will trigger automatically and an EC2 instance will launch $$
