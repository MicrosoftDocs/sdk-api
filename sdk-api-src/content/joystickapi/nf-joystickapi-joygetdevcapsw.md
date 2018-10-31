---
UID: NF:joystickapi.joyGetDevCapsW
title: joyGetDevCapsW function
author: windows-sdk-content
description: The joyGetDevCaps function queries a joystick to determine its capabilities.
old-location: multimedia\joygetdevcaps.htm
tech.root: Multimedia
ms.assetid: 706cab9d-7d04-4151-80df-badd1d446a80
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "_win32_joyGetDevCaps, joGetDevCapsA, joyGetDevCaps, joyGetDevCaps function [Windows Multimedia], joyGetDevCapsW, joystickapi/joGetDevCapsA, joystickapi/joyGetDevCaps, joystickapi/joyGetDevCapsW, multimedia.joygetdevcaps"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: joystickapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: joyGetDevCapsW (Unicode) and joGetDevCapsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winmm.lib
req.dll: Winmm.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-joystick-l1-1-0.dll
 - winmmbase.dll
api_name:
 - joyGetDevCaps
 - joGetDevCapsA
 - joyGetDevCapsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# joyGetDevCapsW function


## -description



The <b>joyGetDevCaps</b> function queries a joystick to determine its capabilities.




## -parameters




### -param uJoyID

Identifier of the joystick to be queried. Valid values for <i>uJoyID</i> range from -1 to 15. A value of -1 enables retrieval of the <b>szRegKey</b> member of the <a href="https://msdn.microsoft.com/9b175aaf-f408-4fe8-bd7c-56f513b57c1b">JOYCAPS</a> structure whether a device is present or not. 


### -param pjc

Pointer to a <a href="https://msdn.microsoft.com/9b175aaf-f408-4fe8-bd7c-56f513b57c1b">JOYCAPS</a> structure to contain the capabilities of the joystick.


### -param cbjc

Size, in bytes, of the <a href="https://msdn.microsoft.com/9b175aaf-f408-4fe8-bd7c-56f513b57c1b">JOYCAPS</a> structure.


## -returns



Returns JOYERR_NOERROR if successful or one of the following error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
The joystick driver is not present, or the specified joystick identifier is invalid. The specified joystick identifier is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter was passed. 

</td>
</tr>
</table>
 




## -remarks



Use the <a href="https://msdn.microsoft.com/dc268db5-da2d-4139-97da-5d56a54287d5">joyGetNumDevs</a> function to determine the number of joystick devices supported by the driver.
      

This method fails when passed an invalid value for the <i>cbjc</i> parameter. 
      




## -see-also




<a href="https://msdn.microsoft.com/29fe25c8-51ea-4dc1-9f98-1c10d23b7b2a">Joysticks</a>



<a href="https://msdn.microsoft.com/84e47ac3-b40f-48bc-8f59-cc678d7d521e">Multimedia Joystick Functions</a>
 

 

