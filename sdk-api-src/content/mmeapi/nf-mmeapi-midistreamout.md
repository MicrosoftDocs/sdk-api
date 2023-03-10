---
UID: NF:mmeapi.midiStreamOut
title: midiStreamOut function (mmeapi.h)
description: The midiStreamOut function plays or queues a stream (buffer) of MIDI data to a MIDI output device.
helpviewer_keywords: ["_win32_midiStreamOut","midiStreamOut","midiStreamOut function [Windows Multimedia]","mmeapi/midiStreamOut","multimedia.midistreamout"]
old-location: multimedia\midistreamout.htm
tech.root: Multimedia
ms.assetid: f2ebc646-7d8b-4fde-a6fc-2455b02d3d8b
ms.date: 12/05/2018
ms.keywords: _win32_midiStreamOut, midiStreamOut, midiStreamOut function [Windows Multimedia], mmeapi/midiStreamOut, multimedia.midistreamout
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
 - midiStreamOut
 - mmeapi/midiStreamOut
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
 - midiStreamOut
---

# midiStreamOut function


## -description

The <b>midiStreamOut</b> function plays or queues a stream (buffer) of MIDI data to a MIDI output device.

## -parameters

### -param hms

Handle to a MIDI stream. This handle must have been returned by a call to the <a href="/previous-versions/dd798486(v=vs.85)">midiStreamOpen</a> function. This handle identifies the output device.

### -param pmh

Pointer to a <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure that identifies the MIDI buffer.

### -param cbmh

Size, in bytes, of the <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure.

## -returns

Returns MMSYSERR_NOERROR if successful or an error otherwise. Possible error values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
The system is unable to allocate or lock memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MIDIERR_STILLPLAYING</b></dt>
</dl>
</td>
<td width="60%">
The output buffer pointed to by <i>lpMidiHdr</i> is still playing or is queued from a previous call to <a href="/previous-versions/dd798487(v=vs.85)">midiStreamOut</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MIDIERR_UNPREPARED</b></dt>
</dl>
</td>
<td width="60%">
The header pointed to by <i>lpMidiHdr</i> has not been prepared.

</td>
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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The pointer specified by <i>lpMidiHdr</i> is invalid.

</td>
</tr>
</table>

## -remarks

Before the buffer is passed to <a href="/previous-versions/dd798486(v=vs.85)">midiStreamOpen</a>, it must be prepared by using the <a href="/previous-versions/dd798477(v=vs.85)">midiOutPrepareHeader</a> function.

Because the <a href="/previous-versions/dd798486(v=vs.85)">midiStreamOpen</a> function opens the output device in paused mode, you must call the <a href="/previous-versions/dd798491(v=vs.85)">midiStreamRestart</a> function before you can use <b>midiStreamOut</b> to start the playback.

For the current implementation of this function, the buffer must be smaller than 64K.

The buffer pointed to by the <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure contains one or more MIDI events, each of which is defined by a <a href="/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a> structure.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>