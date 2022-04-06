# DPOE-N-Workshop_IntroCLI

# Overview

This single-day free webinar provides an introduction to the command line interface (CLI) and a few tools for digital preservation with a focus on audiovisual assets. It's provided by the Digital Preservation Outreach & Education Network (DPOE-N), part of the Pratt Institute's School of Information and New York University's Moving Image Archiving Program (MIAP).

See [this link](https://www.dpoe.network/workshops/) for more info about DPOE-N workshops

The presentation slides can be accessed at [this link](https://brnco.github.io/DPOE-N-Workshop_IntroCLI-AVTools/webinar.html)

# Table of Contents

[Course Description](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#course-description)

[Tools list](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#command-line-software-discussed)

[Readings and Resources](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#readings--resources)

[Agenda](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#agenda)

[Install Instructions](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#install-instructions)

  - [Mac / Homebrew](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#mac-setup-instructions)
  - [Windows / WSL](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#windows-setup-instructions)
  - [Tools](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#install-tools)

[Presenter Bio](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#presenter-bio)

[Acknowledgements](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#acknowledgements)

# Course Description

# Command-Line Software Discussed

While not an exhaustive list, the webinar will touch on some fundamental software to managing digital files, with an emphasis on audiovisual formats.

These tools include:

[bash](https://www.gnu.org/software/bash/)

[rsync](https://rsync.samba.org/)

[md5sum](https://linux.die.net/man/1/md5sum) + [shasum](https://linux.die.net/man/1/shasum)

[BagIt](https://datatracker.ietf.org/doc/html/rfc8493) + [grabbags](https://github.com/amiaopensource/grabbags)

[MediaInfo](https://mediaarea.net/en/MediaInfo)

[ffmpeg](http://ffmpeg.org/)

# Readings & Resources

[Programming is Forgetting: Toward a New Hacker Ethic](http://opentranscripts.org/transcript/programming-forgetting-new-hacker-ethic/) by Allison Parrish

[Heroes in a Bash Shell](https://www.redhat.com/en/command-line-heroes/season-3/heroes-in-a-bash-shell) by Command Line Heroes

[Script Ahoy](https://dd388.github.io/crals/) - a bash helper for archivists by Dianne Dietrich and Jarret Drake

[Bash for Archivists](https://reto.ch/training/2020/202006/) - an intro course by Reto Kromer

[ffmprovisr](https://amiaopensource.github.io/ffmprovisr/) - an ffmpeg helper maintained by [Ashley Blewer](https://ashleyblewer.com/)

[Man Pages](https://en.wikipedia.org/wiki/Man_page) - the Wikipedia page for "man pages" aka manual pages, describing the history and use of manual pages in the command line

# Agenda

## Part 1 - History, Context, Objectives

what the command line is, what we can do with it, why it matters

## Part 2 - Intro to Commands

basic structures, navigation, inputs & outputs

## LUNCH

## Part 3 - CLI Tools for Digital Preservation

moving files, verifying integrity of files and metadata

## Part 4 - CLI Tools for Audiovisual Formats

media file structure, MediaInfo + ffmpeg

## Part 5 - Intro to Scripting

workflow setup, variables, loops, managing scripts

# Install instructions

## Test Files

Please download a set of test file sthat you'll use for both days 1 and 2 [at this link](https://drive.google.com/drive/folders/1QqII7T8oRvwAVdBmZjcNh5DlDc93tR6s?usp=sharing)

## Mac Setup Instructions

Macs ship with an application named “Terminal” which is their default command line interface. It will work great for this webinar, you may even see me using at some point.

We will be using something called a “package manager” to install the software tools we’re demo-ing. Package managers help people manage their software without the use of “installers” like you might be used to, they’re very common on Linux.

Once you have installed the package manager, Homebrew, proceed to the [tools install section](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#install-tools)

### Install Homebrew

For Mac, the package manager we’ll be using is called Homebrew. If you have administrative access to your machine, you can install homebrew with [the steps on their website](https://brew.sh) (it’s a Terminal command).

If you don't have admin access on your Mac, you can still install Homebrew and the other tools for this workshop by using the below steps.

1. Open Terminal
  - type `Cmd + Space` to search your mac
  - type `terminal` and press enter
2. In Terminal, navigate to your home folder
  - type `cd ~/` and press enter
3. install Homebrew in your home folder
  - type the below and press enter
  - `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"` and press enter
4. Once that command completes, go to Terminal -> Preferences -> Shell
  - In the "Startup" Section, check the box to "Run Command"
  - type this command into the box `export PATH=$PATH:${HOME}/brew/bin`
  - Check the box to "Run inside shell"

With either install method, you can check if your install was successful by opening Terminal and typing `brew help` - if you get help output, you're good; if you get an error, email me.


## Windows setup instructions

This workshop is based on the BASH programming language/ shell, which is not available by default on Windows as it is on Mac. Windows uses a proprietary command-line interface referred to cmd.exe, originally released in 1993. It’s like bash in its operation but there are many, many syntactical and technical differences. While I have experience scripting on Windows, it was how I initially learned most of this, those skills are not very sharp at this time and I just don’t think I can support you at the level I’d need to in this workshop.

That being said, you are welcome to follow along in CMD and make the modifications necessary, if you’d like.

Otherwise, we’re going to install bash on your Windows machine, through the Windows subsystem for Linux (WSL). WSL is like having Linux installed, except without the headache of partitioning discs or creating bootable disc images - it’s Linux running as a Microsoft Windows application. It’s an official Windows software, so you can trust it at the same level you trust anything from them.

With WSL installed, we will then use the Ubuntu Linux package manager, apt-get, to install software.

Once you have installed WSL, proceed to the [tools install section](https://github.com/brnco/DPOE-N-Workshop_IntroCLI-AVTools#install-tools)

### Install Windows Subsystem for Linux (WSL)

To install WSL, follow [the instructions on the Microsoft website](https://docs.microsoft.com/en-us/windows/wsl/install-win10)

[Here is a great video](https://www.youtube.com/watch?v=X-DHaQLrBi8) describing the steps, as well

## Install tools

This section assumes that you have completed the above steps to install Homebrew/ WSL

This software is installed entirely via the command line. Each command is written on its own line and will appear formatted `like this`. Type the command in exactly as you see it here and press enter after each command.

### ffmpeg

ffmpeg is one of the most important and widely-used software projects on earth - it’s the backbone of Netflix and Facebook streaming services, as well as VLC. ffmpeg helps people stream, transcode, and investigate audiovisual media files.

#### Mac

`brew install ffmpeg`

#### WSL

Choose one of the following options

`apt-get install ffmpeg`

Note that I haven't tested every functionality of the above ffmpeg build. There may be commands which won't work due to licensing issues with non-free formats (notably H.264 and mp3). The below build is ~probably better.

`sudo add-apt-repository ppa:mc3man/trusty-media`

`sudo apt-get update`

`sudo apt-get dist-upgrade`

`sudo apt-get install ffmpeg`

### MediaInfo

MediaInfo creates structured technical metadata from a variety of audiovisual media filetypes, everything from sample rates to listing subtitle tracks.

#### Mac

`brew install mediainfo`

#### WSL

`apt-get install mediainfo`

### grabbags

grabbags is a software tool maintained the Association of Moving Image Archivists Open Source Committee and it helps archivists manage bags in the manner of the Library of Congress’ BagIt specification.

#### Mac

`brew tap amiaopensource/amiaos`

`brew install grabbags`

#### WSL

`cd ~/`

`git clone https://github.com/amiaopensource/grabbags.git`

# Presenter Bio

Brendan Coates is a gardener, musician, proud cat-parent, and member of the Los Angeles Tenants Union. He has been working to ensure the long-term stability and relevance of archival audiovisual materials since 2011, with a particular focus on oral histories, for which he's contributed to programs at The Academy of Motion Picture Arts and Sciences, The History Makers, and, currently, at the Computer History Museum. His background with historical AV also led him to the UCSB Library, where he headed the Special Research Collections digitization lab for four years, contributing to their cylinder program and The National Jukebox projects, among others. A lifelong interest in computers and aversion to boring work inspired him to start learning Bash and Python and integrating them into his professional life, and he's just been on that path ever since. He's a graduate of the University of Michigan's School of Information (#HailToTheVictims), a winner of the James A. Lindner Prize for [QCT-Parse](https://github.com/FutureDays/qct-parse), a winner of the IGF Nuovo Award with [Cassie McQuater](http://cassiemcquater.com/) for his contribution to her web game [Black Room](https://cass.itch.io/blackroom), and an active member of The Association for Moving Image Archivists ([AMIA](https://amianet.org/)) and the Oral History Association's Archives Interest Group ([OHAAIG](https://www.oralhistory.org/oha-archives-interest-group-oha-aig/)).

# Acknowledgements

As a project about open-source software, this presentation is also entirely open source. As such, it is built on top of the work of others, notably:

Lauren Sorensen, who spear-headed this whole thing

Juana Suarez, Jess Cayer, and the team at NYU MIAP - our gracious hosts who spent many hours reviewing applications

Nick Krabbenhoeft and Ben Turkus, who are doing the Day 2 of this series, an intro to Python

Ashley Blewer, Dianne Dietrich, Jarret Drake, Reto Kromer - as mentioned above, these people don't just do good work they also share it

Morgan Morel, my bud who helped brainstorm all this

The presentation framework is reveal.js | all images via me or Wikimedia Commons
