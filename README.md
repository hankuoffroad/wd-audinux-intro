# Writing Day 2024 Audinux - Plan and Publish a User Guide

## Session 1: Onboard new participants 10:30 UTC to 14:00 UTC 22 September 2024

### Introduction to Audinux

Audinux is a repository for FOSS music applications and plugins that are packaged for the Fedora Linux and its variant distributions. Audinux offers free alternatives to VST (Windows) and AU (Mac).
    
### Intended audience

Musicians, Home recording artists, Podcasters, Content creators, Tinkerers with curious mind
    
### Content type

Introductory user guide

### Tools for publication

The GitHub web editor

Git-workflow from your favorite local writing setup and text editor.
    
### End to end processes

Create a fork

Pull request to https://github.com/audinux/audinux.github.io/tree/main/pages/user_guide

### Template: Initial configuration for music creation (Instrument: Electric guitar)

https://github.com/audinux/audinux.github.io/blob/main/pages/user_guide/introduction.md
    
### Audio tools

#### Audio plug-in: digital signal processing or sound synthesis

There are three broad classes of audio plug-in: those which transform existing audio samples, those which generate new audio samples through sound synthesis, and those which analyze existing audio samples.

VAMP: analysis

Apple: Audio Units - Transformation, synthesis

VST: Virtual Studio Technology (Steinberg)

The Linux Audio Developer's Simple Plugin API (LADSPA) is an application programming interface (API) standard for handling audio filters and audio signal processing effects.

LADSPA is an audio effects plugin architecture for filters, reverbs and other sound processing software tools, whereas DSSI was designed specifically for instrument plugins that generate sound from note events. DSSI extends LADSPA by adding note event delivery, but it also adds predefined program selections and a method for plugins to provide their own user interfaces, both of which may also be used by effects plugins.

LV2 (LADSPA Version 2) is a set of royalty-free open standards for music production plug-ins and matching host applications. LV2 compatible software that can host LV2 plug-in bundles includes Ardour, Carla, Calf Stuio Gear, the GStreamer framework and many more. Check the upstream repository - https://gitlab.com/lv2/lv2

Disposable Soft Synth Interface (DSSI)

vst plug-ins: run in any VST3 compliant host/DAW

CLAP: CLever Audio Plug-in or CLAP is an open source software architecture, application programming interface and reference implementation suite for audio effects plugins

CALF Studio Gear: Professional state-of-the-art audio plugins for musicians and multitrack software.

http://calf-studio-gear.org/

Its possible to compile calf plugins under Mac OS X. If you are using homebrew, you can use the Formula from the homebrew-audio tap. This allows you to use calf plugins under any LV2 capable host or via jack using calfjackhost. Be aware that the LV2 GTK dos not work reliably, so you should use the generic UI only.

TAP-plugins:

#### Carla plugin host

cross-platform software: Pre-compiled binaries are available for Linux, macOS and Windows

Carla is available in the KXStudio repositories, Fedora and ArchLinux (all with 'carla' package name).

What does plugin host do?
The program used to dynamically load audio plug-ins is called a plug-in host.

pre-loaded plugins

scan for plugins.
You can configure your plugin folders in the settings if needed. When done, use "Add New Plugin" in the toolbar, then press the "Refresh" button.

Rack:
Plugins are processed in order, from top to bottom.
Plugins with non-stereo audio channels are not supported, but a forced-stereo option is available for Mono ones.

Patchbay:
Modular patchbay mode, just like in JACK Multi-client and many other modular applications.
Every plugin gets its own canvas group and ports allowing you to interconnect plugin audio and MIDI.

notificaion bar: xruns

#### JUCE framework: JUCE is the most widely used framework for audio application and plug-in development.

Using JUCE also future-proofs your products against operating system and plug-in host updates.

https://forum.juce.com/

#### Synth

https://github.com/ardura/Actuate

#### PipeWire and WirePlumber

https://static.sched.com/hosted_files/osseu2024/9e/ELCE2024_Embedded-Audio-Policies-with-WirePlumber.pdf?_gl=1*foeej2*_gcl_au*OTE2NDk0OTA0LjE3MjY0MTE0NTc.*FPAU*OTE2NDk0OTA0LjE3MjY0MTE0NTc

#### MIDI

#### DSP

#### Audio synthesis and analysis

### Reference book

Home Studio Recording - The Complete Guide, Warren Huart and Jerry Hammack

https://homestudiorecording.com/
