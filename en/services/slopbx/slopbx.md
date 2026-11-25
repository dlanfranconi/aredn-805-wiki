---
title: San Luis Obispo County MeshPhone PBX
description: ''
published: true
date: '2026-03-16T04:30:42.874Z'
tags: []
editor: visual
dateCreated: '2026-01-06T08:59:27.392Z'
---

## MeshPhone Information

The MeshPhone network was started by Mark Henderson, N2MH in an attempt to create a unified dialing plan and method to connect various PBXs on the AREDN network together.

  
This effort was then continued by Gerard Hickey, WT0F, to help create a more updated database, as well as adding in the capability for the network to be self healing by checking for PBX trunk status hourly and dynamically generating new routing tables to other connected PBXs as needed. The main network topology is as follows:

-   A local PBX supplying a sip extension and dial tone to a number of users in the area.
-   A network service that links together a number of other pbx's out on the Mesh with a common dial plan among everyone. This allows anyone on the network to call anyone else on the network by dialing 7 digits. This 7-digit number is called a "MeshPhone Number" and is the same number anywhere on the network. The first 3 digits of your MeshPhone Number is your Area Code (in the US and Canada) or 1 plus your 2-digit country code outside of the US and Canada. The last 4-digits is your local PBX extension.

### **Signup --->**[**HERE**](https://forms.gle/CFDgQqcqf3ZgNazb8) **<----**

Use the form to signup for a Line or Conference on the PBX. You will be provided with a extension # and password. 

Your extension number is your User Name when setting up your phone!!!  
  
For a list of supported phones please see the [Supported Devices](https://wiki.aredn805.net/en/Services/SLOPBX/Supported-Phones) list.

### PBX  Server Info 

-   SLO-PBX has the branch office extension of [**80510.**](http://wt0f-meshphone.local.mesh/meshphone/681e3295130f04fe1e065282) The area code is 805, and then the 4 digit local dialing plan is broken up into 3 sections.
    -   10XX: This is reserved for conference rooms or for repeater links over [Asterisk](https://www.asterisk.org/)/[AllStar](https://www.allstarlink.org/)
    -   11XX: This is reserved for individual user extensions on the network
    -   19XX: This is reserved for club shack extensions and EOC extensions.

The SLO PBX belongs to the [MeshPhone](http://wt0f-meshphone.local.mesh/network_map.html) network. The PBX was setup and is currently maintained by W6DGE.

|     |     |
| --- | --- |
| Server admin: | [http://w6bhz-slo-pbx.local.mesh/admin](http://w6bhz-slo-pbx.local.mesh/admin/config.php) |
| Server DNS: | w6bhz-slo-pbx.local.mesh |
| IP: | [10.82.125.198](10.82.125.198) |
| Transport Type: | UDP |
| PJSIP port: | 5060 (preferred) |
| SIP port: | 5160 |
| Codec: | G711u, G729a, G722 |
| Local dial plan: | (\*xx\|1\[0-9\]xx\|7\[0-6\]\|77xxxxxxx\|78) |

> ⇒ **NOTE:** There are too many VOIP phone and ATA device configurations to list. Please look for help in the myriad AREDN forums on the Web or #pbx-networking-voip-meshphone in the ARDEN Community Slack. Also, YouTube is your friend. Check out [FreePBX 101 Phone Setup](https://youtu.be/pI3KHSn0ilY?si=GVR6YhfBwWsszx3j). *Thank you!* " ⇐

## Dialing Instructions

From your PBX extension, you can dial people, services, or other Ham voip networks.

### Dialing other MeshPhone users by Extension

If the ham you are trying to call has an extension on this PBX, you can simply dial his 4-digit extension number. A list of extension numbers can be found on the local [WhitePages](http://w6bhz-slo-pbx.local.mesh/whitepages.php). You can see who is actively registered on the [SLO PBX Dashboard](http://slo-grafana.local.mesh:3000/d/integration_asterisk_overview/slo-county-pbx-overview).

If the ham doesn't have an extension on this PBX, or has an extension on another PBX network, refer to the sections below.

### Dialing by Callsign

*Dialing by Callsign* is used to reach any ham on the Mesh who has a phone that is reachable in some way. This includes anyone on this PBX, people who have individual phones that accept direct incoming ip connections, or other groups of hams who have shared access to a common PBX, similar to the SLOPBX*.* Calls to hams not on this PBX have to be pre-provisioned by the system operator of that PBX on a case by case basis and may not be immediately reachable.

To use *Dialing by Callsign*, follow these steps:

1.  Dial **73** and wait for dial tone
2.  Dial the other ham's callsign by using the letters and numbers on the dial pad to match the letters and numbers in his callsign.
3.  Wait for the phone to ring on the other end.

For example, to reach W6DGE, dial 73, wait for dial tone, then dial 96343.

### Dialing by MeshPhone Number

A *MeshPhone Number* consists of an Area Code (NPA) and local extension number. The *MeshPhone Number* is always 7 digits long. In the case where local extension numbers are less than 4 digits, a digit or digits may be prepended to the local extension number to build it out to 4 digits. This is only done for *MeshPhone* purposes.

To use *Dialing by MeshPhone Number*, follow these steps:

1.  Dial **78** and wait for dial tone
2.  Dial the other ham's *MeshPhone Number.*
3.  Wait for the phone to ring on the other end.

For example: My local extension number is 1100 and I live in Area Code 805. Thus, my *MeshPhone Number* is 805-1100.

As a user of *MeshPhone*, your *MeshPhone Number* will be your local Area Code (regardless of where you live) plus your 4-digit extension number. Some differences exist for international locations.

Using a *MeshPhone Number* allows many local numbering plans to coexist with each extension having a unique *MeshPhone Number.* Making all *MeshPhone Numbers* 7 digits long simplifies call processing. Using an Area Code simplifies determining a network code for a location.

**Tip**

If you dial a *MeshPhone Number* and reach an error condition, wait for the whole error message to play. At the end of the message will be an announcement of "Office Code" followed by a number. This "Office Code" in the intercept message will give you an idea of where the call reached the error condition. Each PBX on MeshPhone has a unique Office Code. If you encounter this error please reach out to W6DGE at extension 1100 or via email at [info@aredn805.net](<mail to:info@aredn805.net>) so that the broken path can be found and addressed.

---

## Calling Other Ham VoIP Telephony Networks

MeshPhone has direct connections with other Ham VoIP Telephony networks. These connections enable calling to and from those networks directly to a final extension number. Those networks are:

1.  Hams Over IP
2.  Hamnet in Europe
3.  Hamphone Italia

In addition, there is a way to call someone by their 7-digit DMR ID number. This feature is under development at this time and will only work for certain people or networks.

### Hams Over IP

To call someone on *Hams Over IP*, dial **74,** wait for dial tone, then dial the desired HoIP number and wait for the call to go through. If you don't want to wait for the call to go through, dial a "#" at the end of the HoIP number.

### Hamnet (Europe)

To call someone in Europe on *Hamnet* (AMPRnet in Europe), dial **72,** wait for dial tone, then dial the desired Hamnet number and wait for the call to go through. If you don't want to wait for the call to go through, dial a "#" at the end of the Hamnet number. Please note that if the desired number on Hamnet is not reachable, the call will be silently dropped.

### Hamphone Italia (Italy)

Extensions on *Hamphone Italia are* based on a user's DMR ID number. Please see the next section on dialing by DMR ID.

### DMR ID Number

To call someone by using their 7-digit DMR ID number, dial **70**, wait for dial tone, then dial the person's 7-digit DMR ID. The call should go through after dialing the last digit of the DMR ID. Note that calls to a non-reachable DMR ID may be either dropped or reach some sort of error condition.

---

## Calling Local Services

There are a number of local services available on MeshPhone. To access these services dial the indicated extension number. In general, note that the following numbers are in the form **xx9y.** Replace the "xx" with the first two number of your local PBX. Contact your local PBX operator to confirm what those first two digits should be for your PBX.

### Voice Mail

Nearly every extension on MeshPhone has voice mail. To access your voicemail box, dial the extension number or feature code assigned by your PBX operator. For the SLOPBX, this extension is \*97 to access from your phone, or 98 to access from any other extension. Please note that using 98 will require you to enter your extension number and voicemail password/pin for voicemail access. Please note that the first time you log into your mailbox you will be asked to setup a voicemail greeting by the bot and a pin to use when accessing via \*98.

### Conference Bridge

The conference bridge is on extension **xx93**. When prompted, record your name or callsign. This will be used to announce your entrance into a call or your departure from a call.

### NOAA Weather

Some PBX's. employ a vhf NOAA Weather to receive local weather forecasts and warnings. Extension **xx99** has been reserved for this feature. Contact your PBX operator for more information or availability of this feature.

### Test Numbers

There are a number of utility extensions that can be called to aid you with configuration, network performance, and other things. Simply being able to call these numbers would indicate that your phone configuration is correct. None of these numbers will complete to a person, so they are available 24 hours a day.

**DTMF Test** - Extension **xx91**. When you call this number you will be prompted to enter DTMF digits. When finished entering digits, dial **#**. Alison will read back the DTMF digits she decoded. This is useful if you have trouble getting your dialed DTMF digits through the network. If you do have problems, it is sometimes useful to repeat the test and hold the dialpad keys down a little longer.

**Date and Time** - Extension **xx92**. Dialing this number will give you the local date and time for your PBX.

**Echo Test** - Extension **xx94**. Dialing this number will loop back your audio back to yourself. This is useful for estimating network delay as well as dropouts. It is also useful if you want to talk to yourself. :-\)

**Milliwatt** - Extension **xx95**. Dialing this number will return a steady 1000 Hz tone. This is useful for setting analog levels or for determining network dropouts. It should also be useful for estimating distortion. However, no information is available as to the tone's actual level, frequency, or distortion characteristics.

**3-Tone Slope** - Extension **xx96**. Similar to *milliwatt*, this number will return 3 tones: 300 Hz, 1000 Hz, and 2804 Hz. each lasting for about 10 seconds. This pattern will continue for about 5 minutes. This is useful in the analog world for estimating equalization (audio frequency response) of a circuit.

**PBX Identification** - Extension **xx97**. This number will return a CW message with the PBX identification.

**Extension Identification** - Extension **xx98**. Allison will read back your extension number.

Feel free to dial these number as often as desired.

### **SLOPBX Functions and Extensions (internal)**

This PBX has a number of services including: Voicemail, Conference lines, and MORE!!! (listed below) Using the 4-digit Dial code the function can be reached. All of the functions listed are provided by this PBX. To access another PBX please refer to the [WhitePages](http://w6bhz-slo-pbx.local.mesh/whitepages.php) site.

|     |     |
| --- | --- |
| Dial Code | Functions / Conference Extension |
| 1000 | SLO Main Conference Room |
| 1001 | SLO Backup Conference Room |
| 1002 | SLO TAC Conference Room |
|     |     |
| 1091 | DTMF test |
| 1092 | Date and Time |
| 1093 | MeetMe conference bridge |
| 1094 | Echo test |
| 1095 | Milliwatt (1 KHz tone) |
| 1096 | 3-tone slope (404,1004,3004 Hz tones) |
| 1097 | Switch ID (cw) |
| 1098 | Extension ID readback |
| \*  | Direct Dial Prefix |
| \*\* | In-Call Asterisk Disconnect Code |
| \*0 | Speeddial prefix |
| \*1 | In-Call Asterisk Toggle Call Recording |
| \*10 | Contact Manager Speed Dials |
| \*2 | In-Call Asterisk Attended Transfer |
| \*8 | Asterisk General Call Pickup |
| \*21 | Findme Follow Toggle |
| \*30 | Blacklist a number |
| \*31 | Remove a number from the blacklist |
| \*32 | Blacklist the last caller |
| \*34 | Perform dictation |
| \*35 | Email completed dictation |
| \*36 | Change status to clean for a room. |
| \*37 | Add a product from mini-bar for a room. |
| \*43 | Echo Test |
| \*44 | Send a message number to the receptionist. |
| \*45 | Allow Dynamic Members of a Queue to login or logout. See the Queues Module for how to assign a Dynamic Member to a Queue. |
| \*46 | Queue Pause Toggle |
| \*47 | Playback Queue Caller Count |
| \*52 | Call Forward No Answer/Unavailable Activate |
| \*53 | Call Forward No Answer/Unavailable Deactivate |
| \*54 | User Intercom Allow |
| \*55 | User Intercom Disallow |
| \*60 | Speaking Clock |
| \*65 | Speak Your Extension Number |
| \*68 | Wake Up Calls |
| \*69 | Call Trace |
| \*70 | Call Waiting - Activate |
| \*71 | Call Waiting - Deactivate |
| \*72 | Call Forward All Activate |
| \*73 | Call Forward All Deactivate |
| \*74 | Call Forward All Prompting Deactivate |
| \*75 | Set user speed dial |
| \*76 | DND Toggle |
| \*78 | DND Activate |
| \*79 | DND Deactivate |
| \*8 | Asterisk General Call Pickup |
| \*80 | Intercom prefix |
| \*85 | Pickup ParkedCall Prefix |
| \*86 | Force Park into Private Lot |
| \*87 | Conference Status |
| \*88 | Park to your Assigned Lot |
| \*90 | Call Forward Busy Activate |
| \*91 | Call Forward Busy Deactivate |
| \*92 | Call Forward Busy Prompting Deactivate |
| \*93 | Call Forward All Prompting Activate |
| \*94 | Call Forward Busy Prompting Activate |
| \*95 | Call Forward No Answer/Unavailable Prompting Activate |
| \*96 | Call Forward Toggle |
| \*97 | My Voicemail |
| \*98 | Dial Voicemail |
| ##  | In-Call Asterisk Blind Transfer |
| 555 | ChanSpy |
| 7777 | **Simulate Incoming Call** |

### **SLO-PBX Trunks**

The SLO PBX has trunks to the following stations. Although its only a couple trunks, thanks to the meshphone routing generator freom WT0F, the PBX is able to reach all other users on the mesh via the other PBX trunks that are already in service. You can see more about the PBX servers and trunk routes that exist on this [MAP.](http://wt0f-meshphone.local.mesh/network_map.html)

#### ***\-CUPERTINO, CA 40810 (***[***W6DGE***](http://wt0f-meshphone.local.mesh/meshphone/66f38c387b9165dfa40a89d2)***)***

#### ***\-DAYTON, OH 93710 (***[***NC8Q***](http://wt0f-meshphone.local.mesh/meshphone/65f1b8d32c33475d76c028d1)***)***

#### ***\-NBAM, CA 41560 (***[***KM6AOW***](http://wt0f-meshphone.local.mesh/meshphone/6839d5fccc93d068750afef2)***)***

#### ***\-OTHERS WELCOME!!!***

### INFO

#### [**MeshPhone℠ WhitePages**](http://n2mh-web.local.mesh/meshphone/testnumbers.php) **by N2MH**

#### **MeshPhone database by: Gerard Hickey**

Provides basic telemetry and insights into the MeshPhone network health [\--Link HERE--](http://wt0f-meshphone.local.mesh/)

Call routing is provided with help from the [MeshPhone Generators](https://gitlab.com/aredn-apps/meshphone-generators#differences-between-v1-and-v2-versions)

Maintained by: Gerard Hickey / WTØF hickey@kinetic-compute.com MeshPhone: 386-8611
