---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PHONE_BUTTON_FUNCTION enumeration


## -description


The 
<b>PHONE_BUTTON_FUNCTION</b> enum provides detailed information on a button's function.


## -enum-fields




### -field PBF_UNKNOWN

A "dummy" function assignment that indicates that the exact function of the button is unknown or has not been assigned.


### -field PBF_CONFERENCE

Initiates a conference call or adds a call to a conference call.


### -field PBF_TRANSFER

Initiates a call transfer or completes the transfer of a call.


### -field PBF_DROP

Drops the active call.


### -field PBF_HOLD

Places the active call on hold.


### -field PBF_RECALL

Takes a call off hold.


### -field PBF_DISCONNECT

Disconnects a call, such as after initiating a transfer.


### -field PBF_CONNECT

Reconnects a call that is on consultation hold.


### -field PBF_MSGWAITON

Turns on a message waiting lamp.


### -field PBF_MSGWAITOFF

Turns off a message waiting lamp.


### -field PBF_SELECTRING

Allows the user to select the ring pattern of the phone.


### -field PBF_ABBREVDIAL

Indicates that the number to be dialed will be a short, abbreviated number consisting of one digit or a few digits.


### -field PBF_FORWARD

Initiates or changes call forwarding to this phone.


### -field PBF_PICKUP

Picks up a call ringing on another phone.


### -field PBF_RINGAGAIN

Initiates a request to be notified if a call cannot be completed normally because of a busy signal or no answer.


### -field PBF_PARK

Parks the active call on another phone, placing it on hold there.


### -field PBF_REJECT

Rejects an incoming call before the call has been answered.


### -field PBF_REDIRECT

Redirects an incoming call to another extension before the call has been answered.


### -field PBF_MUTE

Mutes the phone's microphone device.


### -field PBF_VOLUMEUP

Increases the volume of audio through the phone's handset speaker or speakerphone.


### -field PBF_VOLUMEDOWN

Decreases the volume of audio through the phone's handset speaker or speakerphone.


### -field PBF_SPEAKERON

Turns the phone's external speaker on.


### -field PBF_SPEAKEROFF

Turns the phone's external speaker off.


### -field PBF_FLASH

Generates the equivalent of an onhook/offhook sequence. A flash typically indicates that any digits typed next are to be understood as commands to the switch. On many switches, places an active call on consultation hold.


### -field PBF_DATAON

Indicates that the next call is a data call.


### -field PBF_DATAOFF

Indicates that the next call is not a data call.


### -field PBF_DONOTDISTURB

Places the phone in "do not disturb" mode; incoming calls receive a busy signal or are forwarded to an operator or voicemail system.


### -field PBF_INTERCOM

Connects to the intercom to broadcast a page.


### -field PBF_BRIDGEDAPP

Selects a particular appearance of a bridged address.


### -field PBF_BUSY

Makes the phone appear "busy" to incoming calls.


### -field PBF_CALLAPP

Selects a particular call appearance.


### -field PBF_DATETIME

Causes the phone to display the current date and time; this information would be sent by the switch.


### -field PBF_DIRECTORY

Calls up directory service from the switch.


### -field PBF_COVER

Forwards all calls destined for this phone to another phone used for coverage.


### -field PBF_CALLID

Requests display of the caller ID on the phone's display.


### -field PBF_LASTNUM

Redials the last number dialed.


### -field PBF_NIGHTSRV

Places the phone in the mode it is configured for during night hours.


### -field PBF_SENDCALLS

Sends all calls to another phone used for coverage; same as the 
<a href="https://msdn.microsoft.com/33d369d0-2221-403e-8fbc-a9a1cbd640ad">PHONEBUTTONFUNCTION_COVER constant</a>.


### -field PBF_MSGINDICATOR

Controls the message indicator lamp.


### -field PBF_REPDIAL

Repertory dialing—the number to be dialed is provided as a shorthand following the pressing of this button.


### -field PBF_SETREPDIAL

Programs the shorthand-to-phone number mappings accessible by means of repertory dialing (the "REPDIAL" button).


### -field PBF_SYSTEMSPEED

The number to be dialed is provided as a shorthand following the pressing of this button. The mappings for system speed dialing are configured inside the switch.


### -field PBF_STATIONSPEED

The number to be dialed is provided as a shorthand following pressing of this button. The mappings for station speed dialing are specific to this station (phone).


### -field PBF_CAMPON

Camps on an extension that returns a busy indication. When the remote station returns to idle, the phone will be rung with a distinctive pattern. Picking up the local phone reinitiates the call.


### -field PBF_SAVEREPEAT

When pressed while a call or call attempt is active, it will remember that call's number or command. When pressed while no call is active (such as during dial tone), it repeats the most recently saved command.


### -field PBF_QUEUECALL

Queues a call to an outside number after it encounters a trunk-busy indication. When a trunk becomes available later, the phone will be rung with a distinctive pattern. Picking up the local phone reinitiates the call.


### -field PBF_NONE

A "dummy" function assignment that indicates that the button does not have a function.


### -field PBF_SEND

Sends a request for a communications session.


## -see-also




<a href="https://msdn.microsoft.com/a884c0b4-141a-4f04-8cfb-7ae6b1ec11b3">ITPhone::get_ButtonFunction</a>



<a href="https://msdn.microsoft.com/8002ab8a-a15d-4a1f-b0c3-7a15c61cb6c4">ITPhone::put_ButtonFunction</a>
 

 

