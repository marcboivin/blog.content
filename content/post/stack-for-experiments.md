---
title: "Stack for Experiments"
date: 2022-12-19T09:59:08-05:00
draft: false
---

I used to whip up Django anytime I needed a quick web app. Web frontend technologies have gotten messy and complex so I don't enjoy using it as part of my "move fast, test things" workflow. 

My current rules are:

* Terminal is my preferred UI for now;
* Create plain text if I need to read debug;
* Create a XSLX or CSV to analyze data;
* Dump into SQL for more structure stuff;
* Inter process format is JSON.

Good thing APIs are most everywhere and JSON can be used as a backend frontend now. Everybody speaks JSON, you get pretty output everywhere, you can beautify it and put it in plain text, you can easily rework it by hand or by code and the files are relatively small (compared to your XML of old).

I dabble a lot in data and data processing so I keep using Python when I need to publish a simple script or a simple web service in my dev cycle.

## Flask, SQLite and click

I find using Flask keep things light, readable and fast to develop. You add click on top of it and you can get a super quick and nice script with arguments, feedback, interactions. 

SQLite as the data store make for a [great application file format or](https://www.sqlite.org/appfileformat.html) it is also pretty SQL complete so no roadblocks here. Back in the days (2007) you could do SELECT and INSERT but the funkiest of the SQL commands where not supported.

So I don't need to learn new tools and can build on top of this simple yet flexible foundation.

## CSV and Excel 

This is a cluster fuck. Dat science is telling me to setup pipelines and workflows with Airflow and Kafka but I find this very time consuming and since I don't have a specific end goal I don't feel like this is worth my time.

I'm interested in querying CSV as SQL because that would streamline my process, but I didn't find anything Python, able to handle millions of CSV lines AND accept JOIN statements.

I'll definitely [csvsql](https://towardsdatascience.com/analyze-csvs-with-sql-in-command-line-233202dc1241) a try, but my JOIN requirement tells me I should suck it up and make an import script into SQLite. We'll see.

As I write this I see SQLite has a .import function for CSV. Maybe something to test. 

