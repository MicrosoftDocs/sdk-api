---
UID: NF:mmeapi.midiInUnprepareHeader
title: midiInUnprepareHeader function
author: windows-sdk-content
description: The midiInUnprepareHeader function cleans up the preparation performed by the midiInPrepareHeader function.
old-location: multimedia\midiinunprepareheader.htm
tech.root: Multimedia
ms.assetid: d78aa6ab-caa7-44ec-8953-c64613b04430
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_midiInUnprepareHeader, midiInUnprepareHeader, midiInUnprepareHeader function [Windows Multimedia], mmeapi/midiInUnprepareHeader, multimedia.midiinunprepareheader"
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
 - midiInUnprepareHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiInUnprepareHeader function


## -description



The <b>midiInUnprepareHeader</b> function cleans up the preparation performed by the <a href="https://msdn.microsoft.com/26895526-2c1e-4335-8b45-511ca56696ab">midiInPrepareHeader</a> function.




## -parameters




### -param hmi

TBD


### -param pmh

TBD


### -param cbmh

TBD




#### - cbMidiInHdr

Size of the <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure.


#### - hMidiIn

Handle to the MIDI input device.


#### - lpMidiInHdr

Pointer to a <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure identifying the buffer to be cleaned up.


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



This function is complementary to <a href="https://msdn.microsoft.com/26895526-2c1e-4335-8b45-511ca56696ab">midiInPrepareHeader</a>. You must use this function before freeing the buffer. After passing a buffer to the device driver by using the <a href="https://msdn.microsoft.com/b673e252-91d0-45b9-a528-079868b47157">midiInAddBuffer</a> function, you must wait until the driver is finished with the buffer before using <b>midiInUnprepareHeader</b>. Unpreparing a buffer that has not been prepared has no effect, and the function returns MMSYSERR_NOERROR.




## -see-also




<a href="https://msdn.microsoft.com/b3a70441-e8f9-4886-bf22-426ebd74d045">Allocating and Preparing MIDI Data Blocks</a>



<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>
 

 

