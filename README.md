### How to Push KB documents to Zendesk through API


#####*Run this API command to Publish a Document* 

```
curl https://databricks.zendesk.com/api/v2/help_center/sections/115000357886/articles.json \
-d '
{
   "article":{
      "translations":[
         {
            "locale":"en-us",
            "title":"How to create a Test Article Through API",
            "body":"Databricks Test Article",
            "author_id":"Giri Varatharajan",
            "label_names":"Testing",
            "comments_disabled":true,
            "draft":true
         }
      ]
   }
}' \
-v -u userName:passWord -X POST -H "Content-Type: application/json"

```

#####*Make sure you get Rest API Status 201 Created* 

    HTTP/1.1 201 Created
    
#####*Solution:*

Running this curl command directly publishes a document.






