---
UID: NF:mmeapi.midiOutReset
title: midiOutReset function (mmeapi.h)
description: The midiOutReset function turns off all notes on all MIDI channels for the specified MIDI output device.
helpviewer_keywords: ["_win32_midiOutReset","midiOutReset","midiOutReset function [Windows Multimedia]","mmeapi/midiOutReset","multimedia.midioutreset"]
old-location: multimedia\midioutreset.htm
tech.root: Multimedia
ms.assetid: 75abf36d-906f-48d1-b91d-c3fcef586693
ms.date: 12/05/2018
ms.keywords: _win32_midiOutReset, midiOutReset, midiOutReset function [Windows Multimedia], mmeapi/midiOutReset, multimedia.midioutreset
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
 - midiOutReset
 - mmeapi/midiOutReset
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
 - midiOutReset
---

# midiOutReset function


## -description

The <b>midiOutReset</b> function turns off all notes on all MIDI channels for the specified MIDI output device.

## -parameters

### -param hmo

Handle to the MIDI output device. This parameter can also be the handle of a MIDI stream cast to <b>HMIDIOUT</b>.

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

Any pending system-exclusive or stream output buffers are returned to the callback function and the MHDR_DONE flag is set in the <b>dwFlags</b> member of the <a href="/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure.

Terminating a system-exclusive message without sending an EOX (end-of-exclusive) byte might cause problems for the receiving device. The <b>midiOutReset</b> function does not send an EOX byte when it terminates a system-exclusive message - applications are responsible for doing this.

To turn off all notes, a note-off message for each note in each channel is sent. In addition, the sustain controller is turned off for each channel.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>