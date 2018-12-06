---
UID: NF:mmeapi.midiInAddBuffer
title: midiInAddBuffer function
author: windows-sdk-content
description: The midiInAddBuffer function sends an input buffer to a specified opened MIDI input device. This function is used for system-exclusive messages.
old-location: multimedia\midiinaddbuffer.htm
tech.root: Multimedia
ms.assetid: b673e252-91d0-45b9-a528-079868b47157
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_midiInAddBuffer, midiInAddBuffer, midiInAddBuffer function [Windows Multimedia], mmeapi/midiInAddBuffer, multimedia.midiinaddbuffer"
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - midiInAddBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiInAddBuffer function


## -description



The <b>midiInAddBuffer</b> function sends an input buffer to a specified opened MIDI input device. This function is used for system-exclusive messages.




## -parameters




### -param hmi

Handle to the MIDI input device.


### -param pmh

Pointer to a <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure that identifies the buffer.


### -param cbmh

Size, in bytes, of the <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure.


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
The buffer pointed to by <i>lpMidiInHdr</i> is still in the queue.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MIDIERR_UNPREPARED</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpMidiInHdr</i> has not been prepared.

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
</table>
 




## -remarks



When the buffer is filled, it is sent back to the application.

The buffer must be prepared by using the <a href="https://msdn.microsoft.com/26895526-2c1e-4335-8b45-511ca56696ab">midiInPrepareHeader</a> function before it is passed to the <b>midiInAddBuffer</b> function.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 

