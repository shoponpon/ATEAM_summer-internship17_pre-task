# README

<!--This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:
-->

## Versions  
* ruby 2.3.3p222 (2016-11-21 revision 56859) [x86_64-darwin16]
* Rails 5.1.2
<!--
* System dependencies
* Configuration
-->
## Database creation
use mysql,  
```
$ mysql.sever start
$ mysql -u root
mysql> create user 'task-a'@'localhost' identified by 'ateam';
mysql> grant all privileges on *.* to 'task-a'@'localhost';
mysql> exit;
```
and copy two migrate files to ```db```,
```
$ rake db:create
$ rake db:migrate
$ rails g scaffold blogs body:string like:integer created_at:datetime updated_at:datetime --skip-migration
$ rails g scaffold replies blog_id:integer:index comment:string created_at:datetime updated_at:datetime --skip-migration
```
<!--* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...
-->