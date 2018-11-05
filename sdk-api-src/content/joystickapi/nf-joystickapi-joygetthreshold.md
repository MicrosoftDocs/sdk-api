---
UID: NF:joystickapi.joyGetThreshold
title: joyGetThreshold function
author: windows-sdk-content
description: The joyGetThreshold function queries a joystick for its current movement threshold.
old-location: multimedia\joygetthreshold.htm
tech.root: Multimedia
ms.assetid: 17084365-3fb2-422c-97dc-4501aec7a86c
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_joyGetThreshold, joyGetThreshold, joyGetThreshold function [Windows Multimedia], joystickapi/joyGetThreshold, multimedia.joygetthreshold"
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
req.unicode-ansi: 
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
 - joyGetThreshold
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# joyGetThreshold function


## -description



The <b>joyGetThreshold</b> function queries a joystick for its current movement threshold.




## -parameters




### -param uJoyID

Identifier of the joystick. Valid values for <i>uJoyID</i> range from zero (JOYSTICKID1) to 15.


### -param puThreshold

Pointer to a variable that contains the movement threshold value.


## -returns



Returns JOYERR_NOERROR if successful or one of the following error values.

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
The joystick driver is not present.

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



The movement threshold is the distance the joystick must be moved before a joystick position-change message (<a href="https://msdn.microsoft.com/317ac0b2-f873-413d-b071-47d840229643">MM_JOY1MOVE</a>, <a href="https://msdn.microsoft.com/25d98963-03e6-4276-a132-256e8bbfa73b">MM_JOY1ZMOVE</a>, <a href="https://msdn.microsoft.com/8dc1c092-3947-43d5-8504-a4e4e121fbcb">MM_JOY2MOVE</a>, or <a href="https://msdn.microsoft.com/f09a1a11-8c97-4a03-a388-8bf9ab89a3db">MM_JOY2ZMOVE</a>) is sent to a window that has captured the device. The threshold is initially zero.




## -see-also




<a href="https://msdn.microsoft.com/29fe25c8-51ea-4dc1-9f98-1c10d23b7b2a">Joysticks</a>



<a href="https://msdn.microsoft.com/84e47ac3-b40f-48bc-8f59-cc678d7d521e">Multimedia Joystick Functions</a>
 

 

