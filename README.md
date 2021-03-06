# node-saql-poc

Overview 

This POC demonstrates the use of OAuth 2.0 from a client application (node.js app running on Heroku) to connect to Salesforce and submit a SAQL query to the Einstein Analytics API (/wave/query). You will need to create a Connected App app in your Salesforce org and then add the Client Id / Secret as config vars in Heroku:  

Login into Salesforce  
Go to Setup > Apps > App Manager  
Select 'New Connected App'  
Enter Connected App Name: [name]  
Enter API Name: [auto generated from name]  
Email: [your email or an administrative email]  
Select Enable OAuth Settings  
Enter Callback URL: [1 or more callback urls]  
e.g. https://[heroku_app_name].herokuapp.com  
e.g. http://localhost:[port]  
Select Selected OAuth Scope: Full access (full)  
You can review the complete list of scopes here  
Select 'Save'  

The connected app will generate a Client Secret and Client Id, to be used in the client app.  

Client App  

The code for the POC is in the web.js file. The package.json file tells Heroku what dependencies web.js needs.  
