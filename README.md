# bash-hacks

## Overview

This is a collection of bad ideas and simple plasters made of bash that I wrote
because I felt they were convenient at some point. Use them at your own risk! I
haven't got round to checking them for security concerns yet.

Right now, all that's here is:

  * quicksite
  * whatfi

## quicksite

Quicksite assumes you have bash, sudo, and nginx installed. It is a bash script
that sets up a server on a given port, with your current directory as its root,
so that you may easily check that your hacky website is working.

**Intended usage:**

    quicksite -h           # help on how to use the command
    quicksite -c name port # create a site called name on localhost:port
    quicksite -d name port # delete the site called name at localhost:port

In other words, just run `quicksite -c foo 2919` to load your current directory
as the site `foo`, accessible at `localhost:2919`. When you're done testing, it
is a good idea to `quicksite -d foo 2919`. The port number is currently a check
to remind myself I am deleting the right site `foo`, nothing more.

## whatfi

Whatfi scans for available wireless networks around your device so you can find
one to connect to. Currently, the output is one line of text per network. Later
on, the output will be a JSON list that can be transformed for other UI types.

**Intended usage:**

    whatfi                 # performs the iwlist scan and format the output

## Note

Other scripts will be added as I feel like I should write them. Ideas welcome.
