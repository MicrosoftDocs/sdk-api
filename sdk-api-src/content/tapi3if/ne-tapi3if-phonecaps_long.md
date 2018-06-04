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

# PHONECAPS_LONG enumeration


## -description


The 
<b>PHONECAPS_LONG</b> enum is used by methods that set or get phone capabilities described by a long value.


## -enum-fields




### -field PCL_HOOKSWITCHES

Specifies the hookswitch devices available using one or more members of the 
<a href="https://msdn.microsoft.com/20b17e2f-f745-41ef-91ac-d2ab21d43695">PHONE_HOOK_SWITCH_DEVICE</a> enum.


### -field PCL_HANDSETHOOKSWITCHMODES

Specifies the handset hook switch modes.


### -field PCL_HEADSETHOOKSWITCHMODES

Specifies the headset hook switch modes.


### -field PCL_SPEAKERPHONEHOOKSWITCHMODES

Specifies the speakerphone hook switch modes.


### -field PCL_DISPLAYNUMROWS

Specifies the number of rows in a phone display device.


### -field PCL_DISPLAYNUMCOLUMNS

Specifies the number of columns in a phone display device.


### -field PCL_NUMRINGMODES

Specifies the number of ring modes. 




If a USB phone returns zero for this value, the phone typically does not have a ringer device. The ringing sound plays on the default audio device for the system; for example, on sound card speakers.


### -field PCL_NUMBUTTONLAMPS

Specifies the number of button lamps.


### -field PCL_GENERICPHONE

Specifies whether the phone is generic: a value of one indicates it is, a value of zero indicates it is not. 




A generic phone is a phone device that declares itself as available on all addresses that support audio terminals. For example, a USB phone is generic, because it is not tied to a specific TAPI address.


## -see-also




<a href="https://msdn.microsoft.com/9d7804a7-616b-4efc-9f3b-6d7b1fda1bf6">ITPhone::get_PhoneCapsLong</a>
 

 

