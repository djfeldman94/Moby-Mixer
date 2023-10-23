
### Installation

To install MobyMixer server, download the latest release from the [releases page]. The MobyMixer server is currently only available for Windows.
MobyMixer default to installing to `C:\Program Files\MobyMixer`, and communicating on port `64670`, but you can change these parameters during installation.
NOTE: You must use the same port on both the client and server.

To install MobyMixer client, download the MobyMixer app from the Google Play Store. The iOS app is currently in development, and will be available soon.
MobyMixer defaults to communicating on port `64670`, but you can change this in the settings menu.
NOTE: You must use the same port on both the client and server.

## How does MobyMixer work?

MobyMixer uses a client-server architecture. The MobyMixer server runs on the machine you wish to control, and the MobyMixer client
runs on the mobile device you wish to use as a controller. The client and server communicate over a local network connection. At this point,
MobyMixer only supports local network connections, but support for remote connections is planned for the future.

MobyMixer utilizes gRPC for communication between the client and server. gRPC is a high performance, open-source RPC framework developed by Google;
this allows MobyMixer to have extremely responsive controls and low latency.

## Glossary

Some terms used in this document may be unfamiliar to you. Here are some definitions to help you out.

Audio Device
: This refers to an input or output audio device on your PC. For example, your microphone or speakers.

Audio Session
: This refers to an individual application or process that is using an audio device. For example, Discord or Chrome.

Fader
: This refers to an individual slider control. The fader controls the volume of a single Audio Session OR Audio Device.

Group
: This refers to a group of faders. The group controls the volume of multiple Audio Sessions OR Audio Devices. Currently, groups are automatically
created for each Audio Device with all the Audio Sessions that are using that device. Future versions of MobyMixer will allow you to create custom groups.

Main Fader
: Refers to the Fader that controls the volume of all Audio Sessions OR Audio Devices in an Audio Group. Currently, the Main Fader is
always the Audio Device of the auto-generated Audio Group. In future versions of MobyMixer, custom groups will be controlled by a virtual main fader.
