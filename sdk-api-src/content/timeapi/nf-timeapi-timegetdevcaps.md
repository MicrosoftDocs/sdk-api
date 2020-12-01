---
UID: NF:timeapi.timeGetDevCaps
title: timeGetDevCaps function (timeapi.h)
description: The timeGetDevCaps function queries the timer device to determine its resolution.
helpviewer_keywords: ["_win32_timeGetDevCaps","mmsystem/timeGetDevCaps","multimedia.timegetdevcaps","timeGetDevCaps","timeGetDevCaps function [Windows Multimedia]","timeapi/timeGetDevCaps"]
old-location: multimedia\timegetdevcaps.htm
tech.root: Multimedia
ms.assetid: 7b5a9675-1152-4c9e-bc79-fe9afa5c563c
ms.date: 12/05/2018
ms.keywords: _win32_timeGetDevCaps, mmsystem/timeGetDevCaps, multimedia.timegetdevcaps, timeGetDevCaps, timeGetDevCaps function [Windows Multimedia], timeapi/timeGetDevCaps
req.header: timeapi.h
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
 - timeGetDevCaps
 - timeapi/timeGetDevCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-Time-l1-1-0.dll
 - Kernel32.dll
 - Kernel32legacy.dll
api_name:
 - timeGetDevCaps
---

# timeGetDevCaps function


## -description

The <b>timeGetDevCaps</b> function queries the timer device to determine its resolution.

## -parameters

### -param ptc

A pointer to a <a href="/windows/desktop/api/timeapi/ns-timeapi-timecaps">TIMECAPS</a> structure. This structure is filled with information about the resolution of the timer device.

### -param cbtc

The size, in bytes, of the <a href="/windows/desktop/api/timeapi/ns-timeapi-timecaps">TIMECAPS</a> structure.

## -returns

Returns <b>MMSYSERR_NOERROR</b> if successful or an error code otherwise. Possible error codes include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_ERROR</b></dt>
</dl>
</td>
<td width="60%">
General error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TIMERR_NOCANDO</b></dt>
</dl>
</td>
<td width="60%">
The <i>ptc</i> parameter is <b>NULL</b>, or the <i>cbtc</i> parameter is invalid, or some other error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Multimedia/multimedia-timer-functions">Multimedia Timer Functions</a>



<a href="/windows/desktop/Multimedia/multimedia-timers">Multimedia Timers</a>



<a href="/windows/desktop/Multimedia/timer-resolution">Timer Resolution</a>