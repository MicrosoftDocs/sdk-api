---
UID: NF:mmeapi.midiOutUnprepareHeader
title: midiOutUnprepareHeader function (mmeapi.h)
description: The midiOutUnprepareHeader function cleans up the preparation performed by the midiOutPrepareHeader function.
helpviewer_keywords: ["_win32_midiOutUnprepareHeader","midiOutUnprepareHeader","midiOutUnprepareHeader function [Windows Multimedia]","mmeapi/midiOutUnprepareHeader","multimedia.midioutunprepareheader"]
old-location: multimedia\midioutunprepareheader.htm
tech.root: Multimedia
ms.assetid: c36fdd79-afd4-42ce-b251-d0630243af77
ms.date: 12/05/2018
ms.keywords: _win32_midiOutUnprepareHeader, midiOutUnprepareHeader, midiOutUnprepareHeader function [Windows Multimedia], mmeapi/midiOutUnprepareHeader, multimedia.midioutunprepareheader
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
 - midiOutUnprepareHeader
 - mmeapi/midiOutUnprepareHeader
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
 - midiOutUnprepareHeader
---

# midiOutUnprepareHeader function


## -description

The <b>midiOutUnprepareHeader</b> function cleans up the preparation performed by the <a href="/previous-versions/dd798477(v=vs.85)">midiOutPrepareHeader</a> function.

## -parameters

### -param hmo

Handle to the MIDI output device. This parameter can also be the handle of a MIDI stream cast to <b>HMIDIOUT</b>.

### -param pmh

Pointer to a <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure identifying the buffer to be cleaned up.

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
<dt><b>MIDIERR_STILLPLAYING</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpMidiOutHdr</i> is still in the queue.

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
The specified pointer or structure is invalid.

</td>
</tr>
</table>

## -remarks

This function is complementary to the <a href="/previous-versions/dd798477(v=vs.85)">midiOutPrepareHeader</a> function. You must call <b>midiOutUnprepareHeader</b> before freeing the buffer. After passing a buffer to the device driver with the <a href="/previous-versions/dd798474(v=vs.85)">midiOutLongMsg</a> function, you must wait until the device driver is finished with the buffer before calling <b>midiOutUnprepareHeader</b>.

Unpreparing a buffer that has not been prepared has no effect, and the function returns MMSYSERR_NOERROR.

## -see-also

<a href="/windows/desktop/Multimedia/allocating-and-preparing-midi-data-blocks">Allocating and Preparing MIDI Data Blocks</a>



<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>