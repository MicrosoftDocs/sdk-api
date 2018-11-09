---
UID: NF:joystickapi.joySetCapture
title: joySetCapture function
author: windows-sdk-content
description: The joySetCapture function captures a joystick by causing its messages to be sent to the specified window.
old-location: multimedia\joysetcapture.htm
tech.root: Multimedia
ms.assetid: d4511c2c-54b3-48f5-aa30-e198292a4728
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_win32_joySetCapture, joySetCapture, joySetCapture function [Windows Multimedia], joystickapi/joySetCapture, multimedia.joysetcapture"
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
 - joySetCapture
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# joySetCapture function


## -description



The <b>joySetCapture</b> function captures a joystick by causing its messages to be sent to the specified window.




## -parameters




### -param hwnd

Handle to the window to receive the joystick messages.


### -param uJoyID

Identifier of the joystick to be captured. Valid values for <i>uJoyID</i> range from zero (JOYSTICKID1) to 15.
          


### -param uPeriod

Polling frequency, in milliseconds.


### -param fChanged

Change position flag. Specify <b>TRUE</b> for this parameter to send messages only when the position changes by a value greater than the joystick movement threshold. Otherwise, messages are sent at the polling frequency specified in <i>uPeriod</i>.


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
Invalid joystick ID or hwnd is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>JOYERR_NOCANDO</b></dt>
</dl>
</td>
<td width="60%">
Cannot capture joystick input because a required service (such as a Windows timer) is unavailable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>JOYERR_UNPLUGGED</b></dt>
</dl>
</td>
<td width="60%">
The specified joystick is not connected to the system.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>JOYERR_PARMS</b></dt>
</dl>
</td>
<td width="60%">
Invalid joystick ID or hwnd is <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



If the specified joystick is currently captured, the function returns undefined behavior. Call the <a href="https://msdn.microsoft.com/deb1f280-12bd-4e4d-841a-667b7785207c">joyReleaseCapture</a> function to release the captured joystick, or destroy the window to release the joystick automatically.




## -see-also




<a href="https://msdn.microsoft.com/29fe25c8-51ea-4dc1-9f98-1c10d23b7b2a">Joysticks</a>



<a href="https://msdn.microsoft.com/84e47ac3-b40f-48bc-8f59-cc678d7d521e">Multimedia Joystick Functions</a>
 

 

