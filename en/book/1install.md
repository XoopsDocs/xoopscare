# Introduction

**XoopsCare** is another administrator module that provides the ability to maintain your database (verify, repair, optimize, etc.), execute ad-hoc commands in PHP and SQL, and clean cache and templates folders, remove spammed comments and block spammers, and empty your sessions tables.

The module allows the following operations to be run, manually via the admin interface, and/or automatically (via cron job, configurable by action, every number of days).
* Maintain your database (verify, repair, analyze, and optimize)
* Run MySQL queries
* Execute PHP code
* Clean templates_c and cache folders
* Remove spam comments (based on your censor words)
* Clean sessions

Some of the tasks have been incorporated into the standard Admin Control Panel of XOOPS.

# 1.0 Install/Uninstall

No special measures necessary, follow the standard installation process � extract the module folder into the 

/modules 

directory in your XOOPS installation. Install the module through Admin -> System Module -> Modules.

Detailed instructions on installing modules are available in the [**Chapter 2.12 of our XOOPS Operations Manual**](https://www.gitbook.com/book/xoops/xoops-operations-guide/)

###Update

Updating is easy enough, just replace the module with the new one. This pertains to 1.0 (where I started) to current.

###Configuration

Go to the module preferences and setup things to run as you need them to. If you set a particular function to 0 (zero) days, then it will be disabled. To make this work automatically, you will need to do two things:

1. create a cron job that runs XOOPS_ROOT/modules/xoopscare/cron.php?password=*mypassword *
2. put *mypassword* in the module preferences

Alternatively, if you can't setup a cron job, then you can instead implement the Maintenance block on a page (maybe your home page) instead to be your cron job. 
>![](../assets/info/info.png)Note: the block will not actually show.

You may also change the location of the log file.

