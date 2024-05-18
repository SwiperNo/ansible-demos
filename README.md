# They Not Like Us
<img src="./kdot.webp" alt="They Not Like Us" width="300" height="300">

## Overview

This project is a fun and silly way to simiulate ansible depdencies and it works. We added a bit more to this by adding github actions to kick off the ansible playbook. The playbook, `dependencies-example.yml`, calls the ansible role "They". This is my attempt to add a little bit of comedy from recent track from Kedrick Lamar's "They not like us". When the playbook execute successfully, it will print this message. Clone and have fun!


## Dependency location
If you inspect the ansible role for "they" and check the meta directory, ansible dependencies are added here. Here is an example below:

roles/they/
├── defaults
│   └── main.yml
├── files
├── handlers
│   └── main.yml
├── meta
│   └── main.yml


dependencies: 
  - role: roles/not
  - role: roles/like
  - role: roles/us

## Importance of dependencies in Ansible
Depending on your project, there may be times where you need to include a role that sets set up the environment for your application. For example, maybe we need to install java jdk, and you have a role that already configure this, specifically for your enviornment. Instead of writing this again, we can include this as a dependency to run beforce configuring your application. A very simple use case, but the ability to do so is there. 
