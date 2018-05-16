# How to create a synchronization proxy with SyncProxy
This tutorial will show you to how to setup a synchronization proxy with SyncProxy to enable bidirectional, real time reactive synchronization between your backend database (MySQL, SQL Server, MongoDB...) and your offline apps embedding free open source SyncProxy client.

## What is **SyncProxy** ?
>**SyncProxy** is a proxy server that manages all synchronization between a backend database and offline mobile apps. It connects directly to your SQL/NoSQL database to turn it into a real time reactive datasource.

## Customization
**SyncProxy** can be either accessed online or installed on site. This tutorial describes the online use of **SyncProxy**, but it is also perfectly relevant to a custom installation, simply replace **my.syncproxy.com** with your own url.

## To start
First create an account on https://my.syncproxy.com and complete your profile (this is free and takes only one minute). You can later reuse the same account to create other proxies for different apps.
Since you will be the administrator of the proxy, don't forget to check the checkbox "I will manage proxies or groups" and to fill-in your short company info, this will give you access to the admin menu:

![admin menu](https://raw.githubusercontent.com/syncproxy/syncproxy-quickstart/master/admin-menu.png)

## Creating your first proxy
Creating a sync proxy is very easy: just click "New proxy" button from the "Proxies" page, then fill-in the database connection settings. Check the connection with "Test connection":

![new proxy](https://raw.githubusercontent.com/syncproxy/syncproxy-quickstart/master/new-proxy.png)

>**Important**: make sure your firewall is set correctly to accept the connection using the listening port of your database server.

## Discovering the schema
Once your have checked database connection, select the proxy from the list in the admin menu, then click to "Database schema":

![select proxy](https://raw.githubusercontent.com/syncproxy/syncproxy-quickstart/master/select-proxy.png)

The discovered schema looks like below. Simply select the tables and columns you want to sync, and save your schema once you are done.

![schema](https://raw.githubusercontent.com/syncproxy/syncproxy-quickstart/master/schema.png)

## Preparing the database for reactive syncs
**SyncProxy** will add a bunch of structures to your database (depending on your database type: tables, triggers, stored procedures...) that will optimize change detection and enable real time reactive sync.

> To prepare specific **SyncProxy** structures in your database, simply click "Prepare database" button in the Database schema page.

## Creating a group and inviting users to join

To enable users to sync, you will create a group to which a sync profile will be associated (more on this below), then invite users to join. 
> From the admin menu, click on "Groups" and click on "New group".  

This will open the Group page:

![group](https://raw.githubusercontent.com/syncproxy/syncproxy-quickstart/master/group.png)

> Give a friendly name to the group, the click on "Users":
![group users](https://raw.githubusercontent.com/syncproxy/syncproxy-quickstart/master/group-users.png)

## Links
To access **SyncProxy** administration to setup your sync proxy and connect to your backend database, go to www.syncproxy.com.  
Also have a look at the [Quick start guide for Ionic](https://github.com/SyncProxy/syncproxy-quickstart-ionic) which explains how to easily add sync client to your mobile apps.
