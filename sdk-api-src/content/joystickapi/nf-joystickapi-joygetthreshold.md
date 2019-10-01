---
UID: NF:joystickapi.joyGetThreshold
title: joyGetThreshold function (joystickapi.h)
author: windows-sdk-content
description: The joyGetThreshold function queries a joystick for its current movement threshold.
old-location: multimedia\joygetthreshold.htm
tech.root: Multimedia
ms.assetid: 17084365-3fb2-422c-97dc-4501aec7a86c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_joyGetThreshold, joyGetThreshold, joyGetThreshold function [Windows Multimedia], joystickapi/joyGetThreshold, multimedia.joygetthreshold"
ms.topic: function
f1_keywords: 
 - "joystickapi/joyGetThreshold"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



The movement threshold is the distance the joystick must be moved before a joystick position-change message (<a href="https://docs.microsoft.com/windows/desktop/Multimedia/mm-joy1move">MM_JOY1MOVE</a>, <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mm-joy1zmove">MM_JOY1ZMOVE</a>, <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mm-joy2move">MM_JOY2MOVE</a>, or <a href="https://docs.microsoft.com/windows/desktop/Multimedia/mm-joy2zmove">MM_JOY2ZMOVE</a>) is sent to a window that has captured the device. The threshold is initially zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>
 

 

