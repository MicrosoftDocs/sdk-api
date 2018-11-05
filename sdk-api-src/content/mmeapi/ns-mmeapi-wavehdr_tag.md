---
UID: NS:mmeapi.wavehdr_tag
title: wavehdr_tag
author: windows-sdk-content
description: The WAVEHDR structure defines the header used to identify a waveform-audio buffer.
old-location: multimedia\wavehdr.htm
tech.root: Multimedia
ms.assetid: be70ae8e-8d8f-4261-bd0e-c6fd7feec520
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*LPWAVEHDR, *NPWAVEHDR, *PWAVEHDR, LPWAVEHDR, LPWAVEHDR structure pointer [Windows Multimedia], WAVEHDR, WAVEHDR structure [Windows Multimedia], WHDR_BEGINLOOP, WHDR_DONE, WHDR_ENDLOOP, WHDR_INQUEUE, WHDR_PREPARED, _win32_WAVEHDR_str, mmeapi/LPWAVEHDR, mmeapi/WAVEHDR, multimedia.wavehdr, wavehdr_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmeapi.h
api_name:
 - WAVEHDR
product: Windows
targetos: Windows
req.typenames: WAVEHDR, *PWAVEHDR, *NPWAVEHDR, *LPWAVEHDR
req.redist: 
---

# wavehdr_tag structure


## -description



The <b>WAVEHDR</b> structure defines the header used to identify a waveform-audio buffer.




## -struct-fields




### -field lpData

Pointer to the waveform buffer.
          


### -field dwBufferLength

Length, in bytes, of the buffer.
          


### -field dwBytesRecorded

When the header is used in input, specifies how much data is in the buffer.
          


### -field dwUser

User data.
          


### -field dwFlags

A bitwise <b>OR</b> of zero of more flags. The following flags are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="WHDR_BEGINLOOP"></a><a id="whdr_beginloop"></a><dl>
<dt><b>WHDR_BEGINLOOP</b></dt>
</dl>
</td>
<td width="60%">
This buffer is the first buffer in a loop. This flag is used only with output buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_DONE"></a><a id="whdr_done"></a><dl>
<dt><b>WHDR_DONE</b></dt>
</dl>
</td>
<td width="60%">
Set by the device driver to indicate that it is finished with the buffer and is returning it to the application.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_ENDLOOP"></a><a id="whdr_endloop"></a><dl>
<dt><b>WHDR_ENDLOOP</b></dt>
</dl>
</td>
<td width="60%">
This buffer is the last buffer in a loop. This flag is used only with output buffers.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_INQUEUE"></a><a id="whdr_inqueue"></a><dl>
<dt><b>WHDR_INQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Set by Windows to indicate that the buffer is queued for playback.

</td>
</tr>
<tr>
<td width="40%"><a id="WHDR_PREPARED"></a><a id="whdr_prepared"></a><dl>
<dt><b>WHDR_PREPARED</b></dt>
</dl>
</td>
<td width="60%">
Set by Windows to indicate that the buffer has been prepared with the <a href="https://msdn.microsoft.com/2b99eb91-2cc6-4394-af57-4b1276f08974">waveInPrepareHeader</a> or <a href="https://msdn.microsoft.com/f970c7ed-b9c5-45ce-a59b-dee02359ef82">waveOutPrepareHeader</a> function.

</td>
</tr>
</table>
 


### -field dwLoops

Number of times to play the loop. This member is used only with output buffers.


### -field lpNext

Reserved.


### -field reserved

Reserved.


## -remarks



Use the WHDR_BEGINLOOP and WHDR_ENDLOOP flags in the <b>dwFlags</b> member to specify the beginning and ending data blocks for looping. To loop on a single block, specify both flags for the same block. Use the <b>dwLoops</b> member in the <b>WAVEHDR</b> structure for the first block in the loop to specify the number of times to play the loop.

The <b>lpData</b>, <b>dwBufferLength</b>, and <b>dwFlags</b> members must be set before calling the <a href="https://msdn.microsoft.com/2b99eb91-2cc6-4394-af57-4b1276f08974">waveInPrepareHeader</a> or <a href="https://msdn.microsoft.com/f970c7ed-b9c5-45ce-a59b-dee02359ef82">waveOutPrepareHeader</a> function. (For either function, the <b>dwFlags</b> member must be set to zero.)




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/4ae84ba8-f444-4d9e-adc8-343b4ee764cc">Waveform Structures</a>



<a href="https://msdn.microsoft.com/2b99eb91-2cc6-4394-af57-4b1276f08974">waveInPrepareHeader</a>



<a href="https://msdn.microsoft.com/f970c7ed-b9c5-45ce-a59b-dee02359ef82">waveOutPrepareHeader</a>
 

 

