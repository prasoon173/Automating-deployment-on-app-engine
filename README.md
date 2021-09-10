# Automating-deployment-on-app-engine
Here, I have deployed a simple python app on app engine standard and then automated the deployment using build trigger.

First I created a cloud source repository using terraform. 

wrote simple python app that consists of main.py, requirements.txt, app.yaml file

Then I tested that file locally. If that works, deploy it to app engine using 
      $gloud app create
      $gcloud app deploy
      
      
 Now, write a cloudbuild.yaml file where you specify aruments as gcloud app deploy and timeouts. After that, create a build trigger using console ( choose configuration file as yaml ) .
 
 It's testing time :
    Make some changes in main.py file and commit it to your source repo. Based on that change, Cloud build will be triggered and will execute cloudbuild.yaml file. You could monitor this in History of cloud Build. 
    
 Navigate to App Engine : You will see now two versions of same default service. If you click on versions, you will notice that newly created app is receiving 100 % of traffic.
 
 Henceforth, you have automated the deployment on app engine using cloud build triggers. 
