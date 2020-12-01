---
UID: NF:joystickapi.joyGetPos
title: joyGetPos function (joystickapi.h)
description: The joyGetPos function queries a joystick for its position and button status.
helpviewer_keywords: ["_win32_joyGetPos","joyGetPos","joyGetPos function [Windows Multimedia]","joystickapi/joyGetPos","multimedia.joygetpos"]
old-location: multimedia\joygetpos.htm
tech.root: Multimedia
ms.assetid: 84f6a19b-1573-4e36-8a2b-7c79b12bf8ba
ms.date: 12/05/2018
ms.keywords: _win32_joyGetPos, joyGetPos, joyGetPos function [Windows Multimedia], joystickapi/joyGetPos, multimedia.joygetpos
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
 - joyGetPos
 - joystickapi/joyGetPos
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
 - joyGetPos
---

# joyGetPos function


## -description

The <b>joyGetPos</b> function queries a joystick for its position and button status.

## -parameters

### -param uJoyID

Identifier of the joystick to be queried. Valid values for <i>uJoyID</i> range from zero (JOYSTICKID1) to 15.

### -param pji

Pointer to a <a href="/previous-versions/dd757110(v=vs.85)">JOYINFO</a> structure that contains the position and button status of the joystick.

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
</table>

## -remarks

For devices that have four to six axes of movement, a point-of-view control, or more than four buttons, use the <a href="/previous-versions/dd757108(v=vs.85)">joyGetPosEx</a> function.

## -see-also

<a href="/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>