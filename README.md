# DOCUMENTATION OF MY PROJECT
 
## To View Webpage
IP Address: (http://54.229.229.203/)  
Domain Name: (https://afolabivictor.mooo.com/)

## How to Provisioned the Server
* I logged into my AWS Account.
* Clicked on "Instance" at the side bar.  
* Clicked on "Launch Instance" at the top-right corner.  
* Gave my server a name.  
* Chose the Operating System to run on it (Ubuntu server 22.04).
* Chose Instance type (t2 micro).
* Created a "Keypair" that will be used to be connecting to the server.  
* Created Security Group. 
* Configured the storage.
* Then clicked on "Launch Instance".

## How to Install Web Server
* SSH into your server  
* Press the command “sudo apt install nginx”, then press the Enter Key  
* Press the command “systemctl status nginx”, then press the Enter key  
* To run the server, paste the Public ipV4 address on a browser search box  
* If properly installed, it will display WELCOME TO NGINX

## How to Deploy the HTML WebPage
### How to Create the HTML WebPage
* Open VS Code text editor, I created a folder "Second Semester Examination".
* Inside the folder, I created an "index.html" file where I wrote my HTML codes.
* And then, I saved the file.
### How to Create New GitHub Repository and Push Files Into it
* Create a New Repository on your GitUp Account  
* Press the command “cd /path/to/your/folder”     .....#to navigate into your folder directory  
* Press the command “git init”     .....# To Initialize Git repository  
* Press the command “git add .”     .....# To Add all files to the staging area  
* Press the command “git commit -m "Your commit message"”     .....# To add commit message  
* Press the command “git remote add origin https://github.com/Vicktour358/Second-Semester-Examination”     .....# Link to your remote Repo  
* Press the command “git push -u origin main”     .....# Push to the remote repository  
### How to Deploy the HTML WebPage to the Server
* SSH into your server  
* Press the command “cd /var/www/html”     .....#to enter the directory of the web server  
* Press the command “sudo rm index.nginx-debian.html”     .....#to remove the default HTML file from the server directory  
* Press the command “cd ~”     .....#to go to the Home directory  
* Press the command “git clone https://github.com/Vicktour358/Second-Semester-Examination”     .....#to clone GitUp Repository  
* Press the command “cd Second-Semester-Examination”     .....#to enter into the Repo Directory  
* Press the command “sudo mv index.html /var/www/html”     .....#to move desired HTML file to the server directory  

## How to Configured Networking
* Login to your AWS Console  
* Click on “Security Groups” at the side bar (or from Services menu)  
* Click on “Add Rule”  
* Set Rule 1 to: Type --> SSH; Protocol --> TCP; Port --> 22; Source --> Anywhere-IPv4; Description --> SSH Connection  
* Set Rule 2 to: Type --> HTTP; Protocol --> TCP; Port --> 80; Source --> Anywhere-IPv4; Description --> Connect to HTTP  
* Set Rule 3 to: Type --> HTTPS; Protocol --> TCP; Port --> 443; Source --> Anywhere-IPv4; Description --> Connect to HTTPS  
* Click on “Save Rule” 

## Screenshots of my Project
Successful Installation of Web Server (NGINX)
![Installation of Web Server (NGINX)](Screenshots/Nginx.JPG "Successful Installation of Web Server (NGINX)")

Successful Deployment of HTML Web Page
![Loading of Deployed HTML Web Page](Screenshots/Webpage.JPG "Successful Deployment of HTML Web Page")
