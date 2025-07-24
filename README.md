TL;DR Customizing rocker-versioned2 scripts so I can use them to install and configure R and tools on Debian according to my needs

We've been using ml-verse docker images from rocker.org with apptainer on our servers, but apparently they dropped support to the ml-verse image, so we had some people complaining about some old packages not working anymore from inside the "read-only" image. For example, someone trying to install package tikz couldn't do it because of older texlive related packages inside the docker image that couldn't be upgraded.

The main reason we shifted from R on Debian to R from Rocker was that maintaining and updating R on our servers were a little bit demanding... But since ml-verse stopped, people were having trouble installing some packages. So, we're trying to shift back to R on Debian, but installing it from source and configuring it based on what Rocker does with its docker images.


The Dockerfiles and the scripts in this repository are licensed under the GPL 2 or later.
