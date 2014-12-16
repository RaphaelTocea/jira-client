# jira-client #

jira-client is a simple and lightweight JIRA REST client library for Java.

The goal of the project is to provide **simple** and clean English idiomatic expressions for interacting with JIRA. In pursuit of this goal, jira-client lacks the usual verbose and cumbersome contortions often found in Java applications. And since the implementation isn't buried under 57 layers of complicated abstractions, jira-client is easy to extend and debug.

jira-client depends on [Apache HttpComponents](http://hc.apache.org/), [json-lib](http://json.sourceforge.net/), and [joda-time](http://www.joda.org/joda-time/).


## Fork modification ##

this fork add an option to disable hosname verification

you can have a "Java SSLException:hostname in certificate didn't match" if you trying to connect on jira base whitch not supported hostname certificate.

For this you have a new constructor in JiraClient with a boolean to disable verification


 ###Code exemple ###
```
        BasicCredentials creds = new BasicCredentials("batman", "pow! pow!");
        JiraClient jira = new JiraClient("https://jira.example.com/jira", creds, true);
```


