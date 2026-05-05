# Postman API Automation Integration with Github Actions #

This repository is a demostration for POC for integrating postman with the github actions.The Test are written in Postman and they are executed on VM with the help of newman and newman-reporter-htmlextra.
Github Actions will trigger the project execution on every push to the main branch.You can also execute project manually using workflow_disptach.The Project runs on schedule time with the help of the cron job.

The HTML reports is archieved and kept in the artifact section for the team to download it. Along with that they can view reports directly from the github page : https://yogitadaurby-sys.github.io/Phoenix-In-warranty-Flow-Collection/ .
The latest report is mailed to the team member using GMAIL SMTP.

## About Me ##

My name is Yogita Daurby. I have 4.6 year of experience. You can connect with me over :(https://www.linkedin.com/feed/)

## Testing Coverage ##
1. Happy Flow Testing
2. Negative Testing
3. Edge test case testing
4. Token Testing
5. Data driven testing with csv file
6. Schema validation
7. Secretes Management with Github secrets

##  Tech Stack ## 
1. Postman
2. Nodejs-23
3. Newman
4. newman-html-extra
5. Github-actions
6. GMAIL SMTP
7. Githubpages
8. csv for data driven testing
9. AWS EC2 instance for self hosted github runner.

## GitHub Pages ##
You can directly view the latest test report of Postman Test at the GitHub page: https://yogitadaurby-sys.github.io/Phoenix-In-warranty-Flow-Collection/

## HTML Report ##
The report will be created in the newan folder
![Postman Report](https://github.com/yogitadaurby-sys/Phoenix-In-warranty-Flow-Collection/blob/Static-content/Newman_report.png)

## Project structure ##
```
Phoenix Inwarranty Flow Collection
├─ Inwarranty-flow Collection.postman_collection.json # Collection file
├─ QA.postman_environment.json #Environment File
└─ testData.csv # Test Data file

```
   
## How to run the Project ##
You can run the project on your local system. for that:
1. Clone the project on Local System: https://github.com/yogitadaurby-sys/Phoenix-In-warranty-Flow-Collection.git
2. Install Nodejs and NPM from : https://nodejs.org/en
3. Install Newman using ```npm install -g newman```
4. Install Newman-reporter-htmlextra using ``` npm intsall -g newman-reporter-htmlextra ```
5. Run the newman Command :
   
                newman run 'Inwarranty-flow Collection.postman_collection.json' \
               -e QA.postman_environment.json \
               -d testData.csv \
               -r cli,htmlextra \
               --reporter-htmlextra-export ./newman/index.html


               
