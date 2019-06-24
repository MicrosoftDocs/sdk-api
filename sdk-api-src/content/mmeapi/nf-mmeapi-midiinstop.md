---
UID: NF:mmeapi.midiInStop
title: midiInStop function (mmeapi.h)
author: windows-sdk-content
description: The midiInStop function stops MIDI input on the specified MIDI input device.
old-location: multimedia\midiinstop.htm
tech.root: Multimedia
ms.assetid: 2541cfc9-ca65-4156-ae33-c04083556006
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_midiInStop, midiInStop, midiInStop function [Windows Multimedia], mmeapi/midiInStop, multimedia.midiinstop"
ms.topic: function
f1_keywords: ["mmeapi/midiInStop"]
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
 - midiInStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# midiInStop function


## -description



The <b>midiInStop</b> function stops MIDI input on the specified MIDI input device.




## -parameters




### -param hmi

Handle to the MIDI input device.


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



If there are any system-exclusive messages or stream buffers in the queue, the current buffer is marked as done (the <b>dwBytesRecorded</b> member of the <a href="https://docs.microsoft.com/previous-versions/dd798449(v=vs.85)">MIDIHDR</a> structure will contain the actual length of data), but any empty buffers in the queue remain there and are not marked as done.

Calling this function when input is not started has no effect, and the function returns zero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
 

 

