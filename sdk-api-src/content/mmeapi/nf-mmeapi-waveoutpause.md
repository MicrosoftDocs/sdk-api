---
UID: NF:mmeapi.waveOutPause
title: waveOutPause function
author: windows-sdk-content
description: The waveOutPause function pauses playback on the given waveform-audio output device. The current position is saved. Use the waveOutRestart function to resume playback from the current position.
old-location: multimedia\waveoutpause.htm
tech.root: Multimedia
ms.assetid: a54eb1f4-fa80-4995-a70f-1aa480f46e86
ms.author: windowssdkdev
ms.date: 11/12/2018
ms.keywords: "_win32_waveOutPause, mmeapi/waveOutPause, multimedia.waveoutpause, waveOutPause, waveOutPause function [Windows Multimedia]"
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
 - waveOutPause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveOutPause function


## -description



The <b>waveOutPause</b> function pauses playback on the given waveform-audio output device. The current position is saved. Use the <a href="https://msdn.microsoft.com/ca2a1e7c-2399-47d4-8804-41a39f69ec12">waveOutRestart</a> function to resume playback from the current position.




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
<tr>
<td width="40%">
<dl>
<dt><b>MMSYSERR_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Specified device is synchronous and does not support pausing.

</td>
</tr>
</table>
 




## -remarks



Calling this function when the output is already paused has no effect, and the function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

