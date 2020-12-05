# Introduction
Welcome to the "COM3529 Software Testing and Analysis" module at the University
of Sheffield! This repository contains code examples to support the lecture
material, practical sessions, and the assignment.

### Contents

* [Introduction](#introduction)
* [Getting Started](#getting-started)
    * [Using Codio](#using-codio)
    * [Individual Machine Setups](#individual-machine-setups)
    * [Cloning this Repository](#cloning-the-repository)
* [Compiling and Running](#compiling-and-running)
* [Problems or Feedback](#problems-or-feedback)

# Getting Started

We will demonstrate everything using a virtual box on
[Codio](https://www.codio.com), for which you should already have a working
account. All the required tools are already setup for you on Codio, so there is
nothing to do if you are happy to work with your own virtual box there. We give
the instructions for getting started with this in the [next section](#using-codio).

If you prefer to use your own machine, however, you will need to ensure all the
tools we're using in the module are installed and setup on your system. (If I
was taking this module, this is what I would do! For your personal development I
would suggest you at least attempt this.) Unfortunately, however, the teaching
team does not have the resources to give help in setting everything up for each
student's individual machine and configuration. Nevertheless, there is plenty of
online help, pointers to which I give [in the section
below](#individual-machine-setups). 

## Using Codio

Our use of Codio will be limited in that we'll just be using the virtual boxes
for ease of running and using this repository in a standardised setup and
context. To get a box going, go to https://www.codio.com, click the "LOGIN"
button, and login with your university email address and password. Click "My
Projects" under the "BUILD" heading in the left sidebar. Then, click the blue
"New Project" button in the top right. Click "Java 11" as your starting point.
You can name your project whatever you like, but ensure that its visibility
remains "Private". Then click "Create", and you're ready to go. When logging
back into Codio later, you should always see your project listed under "My
Projects".

## Individual Machine Setups

If you intend to use Codio only, you can ignore this section. 

If you intend to set up your own machine for the module, however, you will need
the following:

* __Git__. You will need Git to clone this repository. If you don't already have
  it setup on your machine, you'll need to download and install it. See
  https://git-scm.com/book/en/v2/Getting-Started-Installing-Git.
* __Java 11__. We will be using Java Development Kit (JDK) 11 throughout the
  module, as the most recent long term support (LTS) version of Java released by
  Oracle. However, a more recent JDK should also work fine. Prebuilt OpenJDK
  Binaries are available at https://adoptopenjdk.net. If you already have one
  or more installations of Java on your machine, ensure that a Java 11
  installation (or later) is the default one used at the command line. For
  example, some browsers will install a Java Runtime Environment (JRE) on your
  machine, but this is insufficient for interacting with the code in this
  repository.
* __Maven__. Maven is a build automation tool, package and dependency manager
  for Java. It is available at https://maven.apache.org. 

## Cloning the repository
Open a terminal and change directory to somewhere appropriate on your system.
Then type:

``git clone git@github.com:philmcminn/com3529-code.git``

# Compiling and Running

The code repository for the module uses [Maven](https://maven.apache.org), a
build automation, package and dependency manager for Java. Maven makes it easy
for us to use different tools and libraries (e.g., JUnit) without needing to
download and install them individually, and having to ensure we have updated the
`CLASSPATH` environment variable correctly each time. 

This section will teach you the basic commands needed to get things compiling
and running. For the interested and curious (which testers should be!), there is
more extensive documentation about all the kinds of things you can do with
Maven. See for example Apache's own tutorials at
https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html and
https://maven.apache.org/guides/getting-started/index.html and various
tutorials, for example https://www.tutorialspoint.com/maven/index.htm.

You will notice the repository has a number of top-level directories, e.g.
`lecture-examples`, `assignment`, and so on. Each directory contains code that
needs to be built and run separately using Maven. You can build these via the
command line. If you're using your own machine, you can use an IDE to do this
for you, e.g. [IntelliJ IDEA](https://www.jetbrains.com/idea) or
[Eclipse](https://www.eclipse.org/downloads). However, we will assume that
you're using the command line on Codio. 

For instance to build the code in the examples directory, you first need to
change to that directory in the terminal:

``cd examples``

To compile all the examples, issue the Maven command:

``mvn compile``

To compile all the tests, issue the Maven command:

``mvn test-compile``

To run all of the tests in an individual class:

``mvn -Dtest=PhilTest test``

To run a specific test:

``mvn -Dtest=PhilTest#abEqual test``


# Problems or Feedback

We welcome any feedback or constructive criticism that you may have.

If you have any problems, please contact the module lecturer, Phil McMinn.
Please note that we are limited in the help that we can offer on specific system
setups. If you are experiencing difficulties, please use Codio, where we can
give you full support if you run into problems. 
