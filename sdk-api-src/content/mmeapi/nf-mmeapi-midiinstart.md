---
UID: NF:mmeapi.midiInStart
title: midiInStart function (mmeapi.h)
description: The midiInStart function starts MIDI input on the specified MIDI input device.
helpviewer_keywords: ["_win32_midiInStart","midiInStart","midiInStart function [Windows Multimedia]","mmeapi/midiInStart","multimedia.midiinstart"]
old-location: multimedia\midiinstart.htm
tech.root: Multimedia
ms.assetid: c8d570a2-30a2-453e-a320-7b097c4e90bb
ms.date: 12/05/2018
ms.keywords: _win32_midiInStart, midiInStart, midiInStart function [Windows Multimedia], mmeapi/midiInStart, multimedia.midiinstart
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
 - midiInStart
 - mmeapi/midiInStart
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
 - midiInStart
---

# midiInStart function


## -description

The <b>midiInStart</b> function starts MIDI input on the specified MIDI input device.

## -parameters

### -param hmi

Handle to the MIDI input device.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following

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
The specified device handle is invalid.

</td>
</tr>
</table>

## -remarks

This function resets the time stamp to zero; time stamp values for subsequently received messages are relative to the time that this function was called.

All messages except system-exclusive messages are sent directly to the client when they are received. System-exclusive messages are placed in the buffers supplied by the <a href="/previous-versions/dd798450(v=vs.85)">midiInAddBuffer</a> function. If there are no buffers in the queue, the system-exclusive data is thrown away without notification to the client and input continues. Buffers are returned to the client when they are full, when a complete system-exclusive message has been received, or when the <a href="/previous-versions/dd798461(v=vs.85)">midiInReset</a> function is used. The <b>dwBytesRecorded</b> member of the <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure will contain the actual length of data received.

Calling this function when input is already started has no effect, and the function returns zero.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>