---
UID: NF:mmeapi.midiStreamPause
title: midiStreamPause function (mmeapi.h)
description: The midiStreamPause function pauses playback of a specified MIDI stream.helpviewer_keywords: ["_win32_midiStreamPause","midiStreamPause","midiStreamPause function [Windows Multimedia]","mmeapi/midiStreamPause","multimedia.midistreampause"]
old-location: multimedia\midistreampause.htm
tech.root: Multimedia
ms.assetid: d5e09d45-cfd2-4639-b539-0c6ff03ab3b7
ms.date: 12/05/2018
ms.keywords: _win32_midiStreamPause, midiStreamPause, midiStreamPause function [Windows Multimedia], mmeapi/midiStreamPause, multimedia.midistreampause
f1_keywords:
- mmeapi/midiStreamPause
dev_langs:
- c++
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
- midiStreamPause
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# midiStreamPause function


## -description



The <b>midiStreamPause</b> function pauses playback of a specified MIDI stream.




## -parameters




### -param hms

Handle to a MIDI stream. This handle must have been returned by a call to the <a href="https://docs.microsoft.com/previous-versions/dd798448(v=vs.85)">MIDIEVENT</a> function. This handle identifies the output device.


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



The current playback position is saved when playback is paused. To resume playback from the current position, use the <a href="https://docs.microsoft.com/previous-versions/dd798491(v=vs.85)">midiStreamRestart</a> function.

Calling this function when the output is already paused has no effect, and the function returns MMSYSERR_NOERROR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
 

 

