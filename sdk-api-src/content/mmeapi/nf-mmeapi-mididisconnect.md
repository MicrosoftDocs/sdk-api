---
UID: NF:mmeapi.midiDisconnect
title: midiDisconnect function (mmeapi.h)
description: The midiDisconnect function disconnects a MIDI input device from a MIDI thru or output device, or disconnects a MIDI thru device from a MIDI output device.
helpviewer_keywords: ["_win32_midiDisconnect","midiDisconnect","midiDisconnect function [Windows Multimedia]","mmeapi/midiDisconnect","multimedia.mididisconnect"]
old-location: multimedia\mididisconnect.htm
tech.root: Multimedia
ms.assetid: bf6ea7d0-eb0a-429f-8029-d283808fb85e
ms.date: 12/05/2018
ms.keywords: _win32_midiDisconnect, midiDisconnect, midiDisconnect function [Windows Multimedia], mmeapi/midiDisconnect, multimedia.mididisconnect
req.header: mmeapi.h
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
 - midiDisconnect
 - mmeapi/midiDisconnect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winmm.dll
 - API-MS-Win-mm-mme-l1-1-0.dll
 - winmmbase.dll
api_name:
 - midiDisconnect
---

# midiDisconnect function


## -description

The <b>midiDisconnect</b> function disconnects a MIDI input device from a MIDI thru or output device, or disconnects a MIDI thru device from a MIDI output device.

## -parameters

### -param hmi

Handle to a MIDI input device or a MIDI thru device.

### -param hmo

Handle to the MIDI output device to be disconnected.

### -param pReserved

Reserved; must be <b>NULL</b>.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following:.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
Specified device handle is invalid.

</td>
</tr>
</table>

## -remarks

MIDI input, output, and thru devices can be connected by using the <b>midiConnect</b> function. Thereafter, whenever the MIDI input device receives event data in an MIM_DATA message, a message with the same event data is sent to the output device driver (or through the thru driver to the output drivers).

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>