---
UID: NF:joystickapi.joySetThreshold
title: joySetThreshold function (joystickapi.h)
description: The joySetThreshold function sets the movement threshold of a joystick.
helpviewer_keywords: ["_win32_joySetThreshold","joySetThreshold","joySetThreshold function [Windows Multimedia]","joystickapi/joySetThreshold","multimedia.joysetthreshold"]
old-location: multimedia\joysetthreshold.htm
tech.root: Multimedia
ms.assetid: dc0cdbd1-96a8-4f5f-ba2c-b909a6b6fa0e
ms.date: 12/05/2018
ms.keywords: _win32_joySetThreshold, joySetThreshold, joySetThreshold function [Windows Multimedia], joystickapi/joySetThreshold, multimedia.joysetthreshold
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
 - joySetThreshold
 - joystickapi/joySetThreshold
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
 - joySetThreshold
---

# joySetThreshold function


## -description

The <b>joySetThreshold</b> function sets the movement threshold of a joystick.

## -parameters

### -param uJoyID

Identifier of the joystick. Valid values for <i>uJoyID</i> range from zero (JOYSTICKID1) to 15.

### -param uThreshold

New movement threshold.

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
<dt><b>JOYERR_PARMS</b></dt>
</dl>
</td>
<td width="60%">
The specified joystick device identifier <i>uJoyID</i> is invalid.

</td>
</tr>
</table>

## -remarks

The movement threshold is the distance the joystick must be moved before a joystick position-change message (<a href="/windows/desktop/Multimedia/mm-joy1move">MM_JOY1MOVE</a>, <a href="/windows/desktop/Multimedia/mm-joy1zmove">MM_JOY1ZMOVE</a>, <a href="/windows/desktop/Multimedia/mm-joy2move">MM_JOY2MOVE</a>, or <a href="/windows/desktop/Multimedia/mm-joy2zmove">MM_JOY2ZMOVE</a>) is sent to a window that has captured the device. The threshold is initially zero.

## -see-also

<a href="/windows/desktop/Multimedia/joysticks">Joysticks</a>



<a href="/windows/desktop/Multimedia/multimedia-joystick-functions">Multimedia Joystick Functions</a>