---
UID: NF:joystickapi.joyGetDevCapsW
title: joyGetDevCapsW function (joystickapi.h)
description: The joyGetDevCapsW (Unicode) function queries a joystick to determine its comprehensive capabilities. 
helpviewer_keywords: ["_win32_joyGetDevCaps", "joGetDevCapsA", "joyGetDevCaps", "joyGetDevCaps function [Windows Multimedia]", "joyGetDevCapsW", "joystickapi/joGetDevCapsA", "joystickapi/joyGetDevCaps", "joystickapi/joyGetDevCapsW", "multimedia.joygetdevcaps"]
old-location: multimedia\joygetdevcaps.htm
tech.root: Multimedia
ms.assetid: 706cab9d-7d04-4151-80df-badd1d446a80
ms.date: 08/05/2022
ms.keywords: _win32_joyGetDevCaps, joGetDevCapsA, joyGetDevCaps, joyGetDevCaps function [Windows Multimedia], joyGetDevCapsW, joystickapi/joGetDevCapsA, joystickapi/joyGetDevCaps, joystickapi/joyGetDevCapsW, multimedia.joygetdevcaps
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - joyGetDevCapsW
 - joystickapi/joyGetDevCapsW
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
 - joyGetDevCaps
 - joGetDevCapsA
 - joyGetDevCapsW
---

# joyGetDevCapsW function


## -description

The <b>joyGetDevCaps</b> function queries a joystick to determine its capabilities.

## -parameters

### -param uJoyID

Identifier of the joystick to be queried. Valid values for <i>uJoyID</i> range from -1 to 15. A value of -1 enables retrieval of the <b>szRegKey</b> member of the <a href="/previous-versions/dd757103(v=vs.85)">JOYCAPS</a> structure whether a device is present or not.

### -param pjc

Pointer to a <a href="/previous-versions/dd757103(v=vs.85)">JOYCAPS</a> structure to contain the capabilities of the joystick.

### -param cbjc

Size, in bytes, of the <a href="/previous-versions/dd757103(v=vs.85)">JOYCAPS</a> structure.

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

Use the <a href="/previous-versions/dd757106(v=vs.85)">joyGetNumDevs</a> function to determine the number of joystick devices supported by the driver.
      

This method fails when passed an invalid value for the <i>cbjc</i> parameter. 
      





> [!NOTE]
> The joystickapi.h header defines joyGetDevCaps as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>
