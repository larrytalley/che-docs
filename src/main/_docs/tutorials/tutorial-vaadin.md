---
tags: [ "eclipse" , "che" ]
title: Vaadin
excerpt: ""
layout: tutorials
permalink: /:categories/vaadin/
---
{% include base.html %}
Vaadin is a set of user interface components for Web applications. Vaadin projects work within Che. This page provides a quick configuration guide to get started.

*Instructions - Create a New Workspace*
# Create a new workspace.
# In the dashboard, import a project from source:
https://github.com/mstahv/framework-example

*Instructions - Create Commands*
  
# In the IDE, create a new command. Give it the syntax:
Title:    run
Command:  cd framework-example;mvn package jetty:run
Preview:  http://${server.port.8080}/${current.project.relpath}

# Add a second command of type maven:
Title:    compile
Command:  mvn compile -f ${current.project.path}
Goal:     build
Preview:  <empty>

*Instructions - Test Your Application*
```text  
# Test your application
1. Open src/main/java/org/vaadin/samples/helloworld/*.java
2. Make some edits
3. Run the `run` command.
4. Run the `compile` command.
5. You can refresh the web app in the preview URL to see your changes.

# You can set up live reload and auto-compilation.

