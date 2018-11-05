---
UID: NF:mmeapi.waveOutBreakLoop
title: waveOutBreakLoop function
author: windows-sdk-content
description: The waveOutBreakLoop function breaks a loop on the given waveform-audio output device and allows playback to continue with the next block in the driver list.
old-location: multimedia\waveoutbreakloop.htm
tech.root: Multimedia
ms.assetid: e2cbbd22-09be-4757-a659-94cc6e4a0a5b
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_waveOutBreakLoop, mmeapi/waveOutBreakLoop, multimedia.waveoutbreakloop, waveOutBreakLoop, waveOutBreakLoop function [Windows Multimedia]"
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
 - waveOutBreakLoop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveOutBreakLoop function


## -description



The <b>waveOutBreakLoop</b> function breaks a loop on the given waveform-audio output device and allows playback to continue with the next block in the driver list.




## -parameters




### -param hwo

Handle to the waveform-audio output device.


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
</table>
 




## -remarks



The blocks making up the loop are played to the end before the loop is terminated.

Calling this function when nothing is playing or looping has no effect, and the function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

