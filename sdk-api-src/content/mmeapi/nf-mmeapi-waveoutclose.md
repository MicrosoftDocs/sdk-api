---
UID: NF:mmeapi.waveOutClose
title: waveOutClose function
author: windows-sdk-content
description: The waveOutClose function closes the given waveform-audio output device.
old-location: multimedia\waveoutclose.htm
tech.root: Multimedia
ms.assetid: 582669bf-9a43-453d-9458-9cd4b4dfcb6d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_waveOutClose, mmeapi/waveOutClose, multimedia.waveoutclose, waveOutClose, waveOutClose function [Windows Multimedia]"
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
 - waveOutClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveOutClose function


## -description



The <b>waveOutClose</b> function closes the given waveform-audio output device.




## -parameters




### -param hwo

Handle to the waveform-audio output device. If the function succeeds, the handle is no longer valid after this call.


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
There are still buffers in the queue.

</td>
</tr>
</table>
 




## -remarks



The close operation fails if the device is still playing a waveform-audio buffer that was previously sent by calling <b>waveOutWrite</b>. Before calling <b>waveOutClose</b>, the application must wait for all buffers to finish playing or call the <b>waveOutReset</b> function to terminate playback.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

