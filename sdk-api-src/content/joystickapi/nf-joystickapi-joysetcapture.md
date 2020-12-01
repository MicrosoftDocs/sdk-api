---
UID: NF:joystickapi.joySetCapture
title: joySetCapture function (joystickapi.h)
description: The joySetCapture function captures a joystick by causing its messages to be sent to the specified window.
helpviewer_keywords: ["_win32_joySetCapture","joySetCapture","joySetCapture function [Windows Multimedia]","joystickapi/joySetCapture","multimedia.joysetcapture"]
old-location: multimedia\joysetcapture.htm
tech.root: Multimedia
ms.assetid: d4511c2c-54b3-48f5-aa30-e198292a4728
ms.date: 12/05/2018
ms.keywords: _win32_joySetCapture, joySetCapture, joySetCapture function [Windows Multimedia], joystickapi/joySetCapture, multimedia.joysetcapture
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - joySetCapture
 - joystickapi/joySetCapture
dev_langs:
 - c++
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

If the specified joystick is currently captured, the function returns undefined behavior. Call the <a href="/previous-versions/dd757113(v=vs.85)">joyReleaseCapture</a> function to release the captured joystick, or destroy the window to release the joystick automatically.

## -see-also

<a href="/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>