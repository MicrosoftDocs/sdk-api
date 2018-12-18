---
UID: NF:mmeapi.midiInStart
title: midiInStart function
author: windows-sdk-content
description: The midiInStart function starts MIDI input on the specified MIDI input device.
old-location: multimedia\midiinstart.htm
tech.root: Multimedia
ms.assetid: c8d570a2-30a2-453e-a320-7b097c4e90bb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_midiInStart, midiInStart, midiInStart function [Windows Multimedia], mmeapi/midiInStart, multimedia.midiinstart"
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
 - midiInStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

All messages except system-exclusive messages are sent directly to the client when they are received. System-exclusive messages are placed in the buffers supplied by the <a href="https://msdn.microsoft.com/b673e252-91d0-45b9-a528-079868b47157">midiInAddBuffer</a> function. If there are no buffers in the queue, the system-exclusive data is thrown away without notification to the client and input continues. Buffers are returned to the client when they are full, when a complete system-exclusive message has been received, or when the <a href="https://msdn.microsoft.com/74df14c2-df28-40c0-81f2-aed2147f7072">midiInReset</a> function is used. The <b>dwBytesRecorded</b> member of the <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure will contain the actual length of data received.

Calling this function when input is already started has no effect, and the function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 

