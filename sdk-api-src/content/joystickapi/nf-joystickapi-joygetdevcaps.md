---
UID: NF:joystickapi.joyGetDevCaps
title: joyGetDevCaps function (joystickapi.h)
description: The joyGetDevCaps function queries a joystick to determine its capabilities.helpviewer_keywords: ["_win32_joyGetDevCaps","joGetDevCapsA","joyGetDevCaps","joyGetDevCaps function [Windows Multimedia]","joyGetDevCapsW","joystickapi/joGetDevCapsA","joystickapi/joyGetDevCaps","joystickapi/joyGetDevCapsW","multimedia.joygetdevcaps"]
old-location: multimedia\joygetdevcaps.htm
tech.root: Multimedia
ms.assetid: 706cab9d-7d04-4151-80df-badd1d446a80
ms.date: 12/05/2018
ms.keywords: _win32_joyGetDevCaps, joGetDevCapsA, joyGetDevCaps, joyGetDevCaps function [Windows Multimedia], joyGetDevCapsW, joystickapi/joGetDevCapsA, joystickapi/joyGetDevCaps, joystickapi/joyGetDevCapsW, multimedia.joygetdevcaps
f1_keywords:
- joystickapi/joyGetDevCaps
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# joyGetDevCaps function


## -description



The <b>joyGetDevCaps</b> function queries a joystick to determine its capabilities.




## -parameters




### -param uJoyID

Identifier of the joystick to be queried. Valid values for <i>uJoyID</i> range from -1 to 15. A value of -1 enables retrieval of the <b>szRegKey</b> member of the <a href="https://docs.microsoft.com/previous-versions/dd757103(v=vs.85)">JOYCAPS</a> structure whether a device is present or not. 


### -param pjc

Pointer to a <a href="https://docs.microsoft.com/previous-versions/dd757103(v=vs.85)">JOYCAPS</a> structure to contain the capabilities of the joystick.


### -param cbjc

Size, in bytes, of the <a href="https://docs.microsoft.com/previous-versions/dd757103(v=vs.85)">JOYCAPS</a> structure.


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



Use the <a href="https://docs.microsoft.com/previous-versions/dd757106(v=vs.85)">joyGetNumDevs</a> function to determine the number of joystick devices supported by the driver.
      

This method fails when passed an invalid value for the <i>cbjc</i> parameter. 
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>
 

 

