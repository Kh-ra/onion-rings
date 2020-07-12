# O.R.C.: Onion-Ring Chains

## Introduction / About
This project seeks to create a way to easily manage incoming and outgoing connections with users from hosted content not only as an Onion Service, but also by utilizing higher level "Onion-Ring Chains"--ORCs for short--for additional security and anonymity. 

## What is an Onion-Ring
So, you slice it and then there is usually a wet and dry batt--oh, right.

An "Onion-Ring" is a description of the kind of connection formed between User's and Onion Services. An Onion Service ordinarily advertises itself so that users pass their identity to set introduction points before meeting at a Rendezvous point to exchange content with the Host. This is done through two "Onion-Rings"--the final two Tor circuits that connect the user and the host to the content. This works well, but in the case of exceptionally effective Flow-Correlation Attacks--see DeepCorr--it might be dangerous for the provider of the content to to reveal themselves this way. Our suggestion is chain more Onion-Rings together.

### Kinds of ORCs

#### 2-ORC
This is the standard Onion-Service, where the "Onion-Rings" that are formed are directly between the host of the content and user at the selected rendezvous point, respectively.

#### 4-ORC
This is our primary submission with this project at inception. We provide a way for host's to create a 'Broker Onion-Service'--a BOS--that our user meets with at a rendezvous before then meeting at yet another rendesvous to transfer the message to the host. In this arrangement, the Host appears to be a User utilizing the service, and so can't be distinguished using Flow-Correlation attacks (as easily). Further, the BOS 'forgets' all interactions after occurence, so multiple sites could be hosted through a single front to provide further obfuscation of the host--or potentially each host, if they are distinct--among the now ostensibly larger number of users and the effects that arise from the differences in content being serviced.
This is a 4-ORC because that is the number of Onion-Rings that requests/content travel through: 2 from the host to the BOS, and then 2 from the BOS back to the User.

#### ( n>=6 )-ORC (a.k.a. `Onion-Onion-Rings`)
Coming Soon...

## Features

### 0.1 | Automatically Generate an Onion-Service (to Host Previously Existing Site)
Needs to Be Implemented.

### 0.2 | Automatically Generate BOS for 1 Host
Needs to Be Implemented.

### 1.1 | Make BOS Completely Self-Managing for 1 Host (Implement BOS Life-Cycle)
Needs to Be Implemented.

### 2.1 | Automatically Generate BOS for >1 Host (n-BOS)
Needs to Be Implemented.

### 2.2 | Make n-BOS Completely Self-Managing (Implement n-BOS Life-Cycle)
Needs to Be Implemented.

### More to be Added
