---
UID: NF:mmeapi.midiStreamStop
title: midiStreamStop function (mmeapi.h)
description: The midiStreamStop function turns off all notes on all MIDI channels for the specified MIDI output device.
helpviewer_keywords: ["_win32_midiStreamStop","midiStreamStop","midiStreamStop function [Windows Multimedia]","mmeapi/midiStreamStop","multimedia.midistreamstop"]
old-location: multimedia\midistreamstop.htm
tech.root: Multimedia
ms.assetid: cf91b50c-9be9-49a6-a52c-7a56467ec21a
ms.date: 12/05/2018
ms.keywords: _win32_midiStreamStop, midiStreamStop, midiStreamStop function [Windows Multimedia], mmeapi/midiStreamStop, multimedia.midistreamstop
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
 - midiStreamStop
 - mmeapi/midiStreamStop
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
 - midiStreamStop
---

# midiStreamStop function


## -description

The <b>midiStreamStop</b> function turns off all notes on all MIDI channels for the specified MIDI output device.

## -parameters

### -param hms

Handle to a MIDI stream. This handle must have been returned by a call to the <a href="/previous-versions/dd798486(v=vs.85)">midiStreamOpen</a> function. This handle identifies the output device.

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
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is invalid.

</td>
</tr>
</table>

## -remarks

When you call this function, any pending system-exclusive or stream output buffers are returned to the callback mechanism and the MHDR_DONE bit is set in the <b>dwFlags</b> member of the <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure.

While the <a href="/previous-versions/dd798479(v=vs.85)">midiOutReset</a> function turns off all notes, <b>midiStreamStop</b> turns off only those notes that have been turned on by a MIDI note-on message.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>