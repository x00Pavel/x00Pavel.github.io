---
title: "Personal Projects"
author_profile: true
permalink: /projects
---
 
This page is dedicated to my most interest personal and open source projects I've done during my career in IT.
Projects are grouped by area of IT and type of the application.
> Several projects are team projects where I was a project lead.

---

## Frameworks

### [SCAutolib](https://github.com/x00Pavel/SCAutolib)

Framework for automating testing of smart cards in RHEL/Fedora.
Project was developed from scratch, mostly everything around smart cards testing has to be done if frame of this project by me as an intern.
Testing of smart cards is not so trivial task as it seems to be, because there is no such component in Linux as "smart card".
So testing of this technology requires testing of the whole stack of technologies that makes smart cards work in RHEL/Fedora.

SCAutolib framework provides automated way to setup the system and to provide functionality for testing by itself using virtual smart cards.
From setup perspective, SCAutolib installs/setups required packages and services (like SSSD, OpenSC, SoftHSM2 for virtual card), setups required CA's (local CA, IPA client for already deployed IPA server), adds users to corresponding systems (local system and/or IPA server).
After setup is done, configured services/users/systems can be used in the tests.
Tests ([link](https://github.com/x00Pavel/SC-tests)) are written using [Pytest](https://docs.pytest.org/) testing framework as an executor.

> Currently, the framework undergoing a redesign with better architecture as the first attempt to implement such tool has several drawbacks caused by fewer practical knowledge about the area.

---

## Network

### [SSL Monitor](https://github.com/x00Pavel/SSL-monitor)

Simple CLI application for monitoring SSL communication and provide some basic statics for closed connection.
Can run in two mode: offline processing from pcap file and live capturing.
Implemented in **C** language using PCAP library.

### [HTTP Resolver](https://github.com/x00Pavel/HTTP_resolver)

Implementation of HTTP server that **translates domain name to IPv4/IPv6** address and back.
Also addresses addresses can be read from a file.
Implemented in **Python** language.

### [Packet Sniffer](https://github.com/x00Pavel/Sniffer)

Simple packet sniffer, that sniffers packets on given interface and port.
Output is on the standard output with specific formatting.
Only TCP and UDP packets are supported.
Implemented in **C language using libpcap library**.

---

## Web & Desktop Applications

### [Lunch Web](https://github.com/x00Pavel/lunch-web)

[Link](http://lunch-web.herokuapp.com/) to the page.

Web page for showing menus from local area restaurants.
Implemented as python HTML scrapper using BeautifulSoup framework.
Page by itself is using Pyramid web framework.

### [Management of Festivals](https://github.com/x00Pavel/festival-IS)

[Link](https://festival-is.herokuapp.com/) to the page.

This is a team project were we create a web page for managing and selling the tickets for festivals.
Project is written in Python Flask web framework using Postgres database and running on Heroku.
As an architecture for the page we used MVC pattern.

### [Simulation of Public Transport](https://github.com/x00Pavel/Transport_app)

This is desktop application with interactive GUI.
Applications simulates moving of public transport based on internal clock.
There are some **interactive futures**, such as changing line of transport, changing street congestion, setting time to start from and other.
Implemented in **Java with using JavaFX** package.

---

## Theoretical Informatics

### [Compiler](https://github.com/x00Pavel/IFJ-compiler) & [Interpret](https://github.com/x00Pavel/Interpret) for Pseudo Language

This project contains to parts that were made as two separate projects in the school.
First is a compiler part and the second is an interpret.
Interpret part doesn't strictly follows the compiler part, but just logically complete the whole idea of the interpret that do some work after compiler.

Compiler part was a team project written in **C** language.
There were 3 people in the team.
We split the implementation into smaller sub-parts (such as parser, analyzer, internal code validation, and etc.) between all of us and collaborated on connection points between them to make the compiler work.

Interpret was done as an individual project using Python as a main programming language and PHP for testing.
