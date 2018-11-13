---
UID: NF:mmeapi.midiInPrepareHeader
title: midiInPrepareHeader function
author: windows-sdk-content
description: The midiInPrepareHeader function prepares a buffer for MIDI input.
old-location: multimedia\midiinprepareheader.htm
tech.root: Multimedia
ms.assetid: 26895526-2c1e-4335-8b45-511ca56696ab
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: "_win32_midiInPrepareHeader, midiInPrepareHeader, midiInPrepareHeader function [Windows Multimedia], mmeapi/midiInPrepareHeader, multimedia.midiinprepareheader"
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
 - midiInPrepareHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# midiInPrepareHeader function


## -description



The <b>midiInPrepareHeader</b> function prepares a buffer for MIDI input.




## -parameters




### -param hmi

TBD


### -param pmh

TBD


### -param cbmh

TBD




#### - cbMidiInHdr

Size, in bytes, of the <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure.
          


#### - hMidiIn

Handle to the MIDI input device.
          To get the device handle, call <a href="https://msdn.microsoft.com/230deaef-9473-426f-a0eb-14e259600e68">midiInOpen</a>.


#### - lpMidiInHdr

Pointer to a <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure that identifies the buffer to be prepared.
           

Before calling the function, set the <b>lpData</b>, <b>dwBufferLength</b>, and <b>dwFlags</b> members of the <a href="https://msdn.microsoft.com/630f0645-555e-4f48-9397-2623a9918b8a">MIDIHDR</a> structure. The <b>dwFlags</b> member must be set to zero.
      


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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_INVALPARAM</b></dt>
</dl>
</td>
<td width="60%">
The specified address is invalid.

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



Before you pass a MIDI data block to a device driver, you must prepare the buffer by passing it to the <b>midiInPrepareHeader</b> function. After the header has been prepared, do not modify the buffer. After the driver is done using the buffer, call the <a href="https://msdn.microsoft.com/d78aa6ab-caa7-44ec-8953-c64613b04430">midiInUnprepareHeader</a> function.

The application can re-use the same buffer, or allocate multiple buffers and  call <b>midiInPrepareHeader</b> for each buffer. If you re-use the same buffer, it is not necessary to prepare the buffer each time. You can call  <b>midiInPrepareHeader</b> once at the beginning and then call <a href="https://msdn.microsoft.com/d78aa6ab-caa7-44ec-8953-c64613b04430">midiInUnprepareHeader</a> once at the end.

Preparing a header that has already been prepared has no effect, and the function returns zero.
      




## -see-also




<a href="https://msdn.microsoft.com/b3a70441-e8f9-4886-bf22-426ebd74d045">Allocating and Preparing MIDI Data Blocks</a>



<a href="https://msdn.microsoft.com/9aa9fd79-cd9e-4443-8715-142ea72b82c0">MIDI Functions</a>



<a href="https://msdn.microsoft.com/d78aa6ab-caa7-44ec-8953-c64613b04430">midiInUnprepareHeader</a>
 

 

