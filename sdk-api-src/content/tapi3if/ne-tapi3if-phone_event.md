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

# PHONE_EVENT enumeration


## -description


The 
<b>PHONE_EVENT</b> enum indicates a type of phone event.


## -enum-fields




### -field PE_DISPLAY

Phone display has changed.


### -field PE_LAMPMODE

Lamp mode has changed.


### -field PE_RINGMODE

Ringing mode has changed.


### -field PE_RINGVOLUME

Ringing volume has changed.


### -field PE_HOOKSWITCH

Hookswitch status has changed.


### -field PE_CAPSCHANGE

Phone capabilities have changed.


### -field PE_BUTTON

The phone button has changed.


### -field PE_CLOSE

The phone has been closed.


### -field PE_NUMBERGATHERED

A dialed number has been gathered by the phone.


### -field PE_DIALING

The phone is dialing.


### -field PE_ANSWER

The phone has been answered.


### -field PE_DISCONNECT

The phone has been disconnected.


### -field PE_LASTITEM

Last item in enum. Allows device-specific additions to this enum.


## -see-also




<a href="https://msdn.microsoft.com/01ac0b3f-ba45-4bf3-a0e7-b2c3a5d44727">ITPhoneEvent::get_Event</a>
 

 

