---
UID: NF:mmeapi.midiInUnprepareHeader
title: midiInUnprepareHeader function (mmeapi.h)
author: windows-sdk-content
description: The midiInUnprepareHeader function cleans up the preparation performed by the midiInPrepareHeader function.
old-location: multimedia\midiinunprepareheader.htm
tech.root: Multimedia
ms.assetid: d78aa6ab-caa7-44ec-8953-c64613b04430
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_midiInUnprepareHeader, midiInUnprepareHeader, midiInUnprepareHeader function [Windows Multimedia], mmeapi/midiInUnprepareHeader, multimedia.midiinunprepareheader"
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
 - midiInUnprepareHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# midiInUnprepareHeader function


## -description



The <b>midiInUnprepareHeader</b> function cleans up the preparation performed by the <a href="https://docs.microsoft.com/previous-versions//dd798459(v=vs.85)">midiInPrepareHeader</a> function.




## -parameters




### -param hmi

Handle to the MIDI input device.


### -param pmh

Pointer to a <a href="https://docs.microsoft.com/previous-versions//dd798449(v=vs.85)">MIDIHDR</a> structure identifying the buffer to be cleaned up.


### -param cbmh

Size of the <a href="https://docs.microsoft.com/previous-versions//dd798449(v=vs.85)">MIDIHDR</a> structure.


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
<dt><b>MMSYSERR_INVALHANDLE</b></dt>
</dl>
</td>
<td width="60%">
The specified device handle is invalid.

</td>
</tr>
</table>
 




## -remarks



This function is complementary to <a href="https://docs.microsoft.com/previous-versions//dd798459(v=vs.85)">midiInPrepareHeader</a>. You must use this function before freeing the buffer. After passing a buffer to the device driver by using the <a href="https://docs.microsoft.com/previous-versions//dd798450(v=vs.85)">midiInAddBuffer</a> function, you must wait until the driver is finished with the buffer before using <b>midiInUnprepareHeader</b>. Unpreparing a buffer that has not been prepared has no effect, and the function returns MMSYSERR_NOERROR.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Multimedia/allocating-and-preparing-midi-data-blocks">Allocating and Preparing MIDI Data Blocks</a>



<a href="https://docs.microsoft.com/windows/desktop/Multimedia/midi-functions">MIDI Functions</a>
 

 

