mantiskanban
============

Mantis Kanban that uses ajax and mantisconnect

![Alt text](https://raw.github.com/cgaspard/mantiskanban/master/images/mantis_logo.png "Logo")

Requires Mantis vs 1.2.15 or greater.

JS Configuration: config.js

    Mantis.ConnectURL -  This should point to the mantisconnect.php page on your server. 
        Example: http://example.com/api/soap/mantisconnect.php
        
    Mantis.DefaultFilterID  - ID of the filter you want to load by default.  If null, 
        then it will load the latest filter the user used on the php site.
        
    Mantis.ClosedIssuesFilterID  - Combined with DefaultFilterID issues.  Both sets of 
        issues get loaded into the Kanban.  Allows you to specify a portion of the closed issues to load.
        
    Kanban.NumberOfClosedMessagesToLoad - Limit the number of issues loaded when the 
        ClosedIssuesFilterID is specified


    Default Settings - System will use local storage to save the following items.  Will auto select project based on last project you were logged in under.
    var DefaultSettings = {
        username:"",
        stayLoggedIn:1,
        lastAccessTime:0,
        currentProject:0
    };

Mantis Configuration:

  Scrum Buckets:
  
    If you want to define custom buckets, then in mantis go to Manage > ManageCustomFields.
  
    Then add a field called "ScrumBucket" of type "List" with whatever possible values you want.  Be sure to seperate the
    value with "|" like this: Backlog|Sprint|Current|Design|CodeComplete|Testing|Release
    
    Next you need to associate the custom field with whatever project you want to have it show up on.

  Default Filter:

    You need to setup a filter for project issues.   If you don't, then Mantis will deliver all issues.   When you
    have closed many issues, you will notice the speed greatly decreases.

  Screenshots:

Full Screen:
![Alt text](https://raw.github.com/cgaspard/mantiskanban/master/screenshots/screen1.png "Optional title")

Edit Story:
![Alt text](https://raw.github.com/cgaspard/mantiskanban/master/screenshots/screen2.png "Optional title")

Custom Scrum Buckets:
![Alt text](https://raw.github.com/cgaspard/mantiskanban/master/screenshots/screen3.png "Optional title")

Mantis Statuses as Buckets:
![Alt text](https://raw.github.com/cgaspard/mantiskanban/master/screenshots/screen4.png "Optional title")
