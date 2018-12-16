---
UID: NF:mmeapi.midiStreamStop
title: midiStreamStop function
author: windows-sdk-content
description: The midiStreamStop function turns off all notes on all MIDI channels for the specified MIDI output device.
old-location: multimedia\midistreamstop.htm
tech.root: Multimedia
ms.assetid: cf91b50c-9be9-49a6-a52c-7a56467ec21a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_midiStreamStop, midiStreamStop, midiStreamStop function [Windows Multimedia], mmeapi/midiStreamStop, multimedia.midistreamstop"
ms.topic: function
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
 - midiStreamStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiStreamStop function


## -description



The <b>midiStreamStop</b> function turns off all notes on all MIDI channels for the specified MIDI output device.




## -parameters




### -param hms

Handle to a MIDI stream. This handle must have been returned by a call to the <a href="https://msdn.microsoft.com/355cf034-e1d7-4530-b117-4c505ad0aac6">midiStreamOpen</a> function. This handle identifies the output device.


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



When you call this function, any pending system-exclusive or stream output buffers are returned to the callback mechanism and the MHDR_DONE bit is set in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure.

While the <a href="https://msdn.microsoft.com/75abf36d-906f-48d1-b91d-c3fcef586693">midiOutReset</a> function turns off all notes, <b>midiStreamStop</b> turns off only those notes that have been turned on by a MIDI note-on message.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 

