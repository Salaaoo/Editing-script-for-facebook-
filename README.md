# Editing-script-for-facebook-
This is the code for chnge facebook simple id into prepaid id....



var accountId = require("BusinessUnifiedNavigationContext").adAccountID;
var fb_dtsg = require('DTSGInitialData').token;
var __user = require('CurrentUserInitialData').USER_ID;
fetch("https://business.facebook.com/api/graphql", {
    "headers": {
        "content-type": "application/x-www-form-urlencoded",
    },
    "body": `__a=1&dpr=1&fb_dtsg=${fb_dtsg}&variables=
    {"input":{"billable_account_payment_legacy_account_id":"${accountId}","logging_data":
    {"logging_counter":22,"logging_id":"3418624251"},"recurring_enabled":false,"actor_id":"${__user}","client_mutation_id":"3"}}
    &doc_id=4886770528075857`,
    "method": "POST",
    "mode": "cors",
    "credentials": "include"
 }).then(e => { 
        console.log("__user"); 
location.reload() 
    })
    
    
    
    But i need script to raisa my thershold up!!!!!!!1
