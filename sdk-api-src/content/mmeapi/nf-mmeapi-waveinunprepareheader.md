---
UID: NF:mmeapi.waveInUnprepareHeader
title: waveInUnprepareHeader function
author: windows-sdk-content
description: The waveInUnprepareHeader function cleans up the preparation performed by the waveInPrepareHeader function.
old-location: multimedia\waveinunprepareheader.htm
tech.root: Multimedia
ms.assetid: 13222b09-c58b-461d-85b7-9312a03a888a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_waveInUnprepareHeader, mmeapi/waveInUnprepareHeader, multimedia.waveinunprepareheader, waveInUnprepareHeader, waveInUnprepareHeader function [Windows Multimedia]"
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
 - waveInUnprepareHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveInUnprepareHeader function


## -description



The <b>waveInUnprepareHeader</b> function cleans up the preparation performed by the <a href="https://msdn.microsoft.com/2b99eb91-2cc6-4394-af57-4b1276f08974">waveInPrepareHeader</a> function. This function must be called after the device driver fills a buffer and returns it to the application. You must call this function before freeing the buffer.




## -parameters




### -param hwi

Handle to the waveform-audio input device.


### -param pwh

Pointer to a <a href="https://msdn.microsoft.com/be70ae8e-8d8f-4261-bd0e-c6fd7feec520">WAVEHDR</a> structure identifying the buffer to be cleaned up.


### -param cbwh

Size, in bytes, of the <b>WAVEHDR</b> structure.


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
Specified device handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No device driver is present.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOMEM</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate or lock memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WAVERR_STILLPLAYING</b></dt>
</dl>
</td>
<td width="60%">
The buffer pointed to by the <i>pwh</i> parameter is still in the queue.

</td>
</tr>
</table>
 




## -remarks



This function complements the <b>waveInPrepareHeader</b> function.

You must call this function before freeing the buffer. After passing a buffer to the device driver with the <b>waveInAddBuffer</b> function, you must wait until the driver is finished with the buffer before calling <b>waveInUnprepareHeader</b>. Unpreparing a buffer that has not been prepared has no effect, and the function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

