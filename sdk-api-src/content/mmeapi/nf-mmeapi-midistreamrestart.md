---
UID: NF:mmeapi.midiStreamRestart
title: midiStreamRestart function (mmeapi.h)
description: The midiStreamRestart function restarts a paused MIDI stream.
helpviewer_keywords: ["_win32_midiStreamRestart","midiStreamRestart","midiStreamRestart function [Windows Multimedia]","mmeapi/midiStreamRestart","multimedia.midistreamrestart"]
old-location: multimedia\midistreamrestart.htm
tech.root: Multimedia
ms.assetid: 8d0f31d6-957d-4266-adae-68865466a859
ms.date: 12/05/2018
ms.keywords: _win32_midiStreamRestart, midiStreamRestart, midiStreamRestart function [Windows Multimedia], mmeapi/midiStreamRestart, multimedia.midistreamrestart
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
 - midiStreamRestart
 - mmeapi/midiStreamRestart
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
 - midiStreamRestart
---

# midiStreamRestart function


## -description

The <b>midiStreamRestart</b> function restarts a paused MIDI stream.

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

Calling this function when the output is not paused has no effect, and the function returns MMSYSERR_NOERROR.

## -see-also

<a href="/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>