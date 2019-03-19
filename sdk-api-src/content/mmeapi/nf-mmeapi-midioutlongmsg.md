---
UID: NF:mmeapi.midiOutLongMsg
title: midiOutLongMsg function (mmeapi.h)
author: windows-sdk-content
description: The midiOutLongMsg function sends a system-exclusive MIDI message to the specified MIDI output device.
old-location: multimedia\midioutlongmsg.htm
tech.root: Multimedia
ms.assetid: 7fda802b-eed5-4a27-8bc0-1f43f4722d33
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_midiOutLongMsg, midiOutLongMsg, midiOutLongMsg function [Windows Multimedia], mmeapi/midiOutLongMsg, multimedia.midioutlongmsg"
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
 - midiOutLongMsg
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiOutLongMsg function


## -description



The <b>midiOutLongMsg</b> function sends a system-exclusive MIDI message to the specified MIDI output device.




## -parameters




### -param hmo

Handle to the MIDI output device. This parameter can also be the handle of a MIDI stream cast to <b>HMIDIOUT</b>.


### -param pmh

Pointer to a <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure that identifies the MIDI buffer.


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
<dt><b>MIDIERR_NOTREADY</b></dt>
</dl>
</td>
<td width="60%">
The hardware is busy with other data.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MIDIERR_UNPREPARED</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by <i>lpMidiOutHdr</i> has not been prepared.

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



Before the buffer is passed to <b>midiOutLongMsg</b>, it must be prepared by using the <a href="https://msdn.microsoft.com/3e457f08-a885-48f8-97c1-ba1baef97759">midiOutPrepareHeader</a> function. The MIDI output device driver determines whether the data is sent synchronously or asynchronously.




## -see-also




<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 

