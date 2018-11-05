---
UID: NF:mmeapi.waveOutReset
title: waveOutReset function
author: windows-sdk-content
description: The waveOutReset function stops playback on the given waveform-audio output device and resets the current position to zero. All pending playback buffers are marked as done (WHDR_DONE) and returned to the application.
old-location: multimedia\waveoutreset.htm
tech.root: Multimedia
ms.assetid: 8a057dcd-985b-4ec7-be5b-c1cc2a6d1e72
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "_win32_waveOutReset, mmeapi/waveOutReset, multimedia.waveoutreset, waveOutReset, waveOutReset function [Windows Multimedia]"
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
 - waveOutReset
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveOutReset function


## -description



The <b>waveOutReset</b> function stops playback on the given waveform-audio output device and resets the current position to zero. All pending playback buffers are marked as done (WHDR_DONE) and returned to the application.




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



After this function returns, the application can send new playback buffers to the device by calling <a href="https://msdn.microsoft.com/d687b136-8ce3-43fc-b459-b12a3fe862c8">waveOutWrite</a>, or close the device by calling <a href="https://msdn.microsoft.com/582669bf-9a43-453d-9458-9cd4b4dfcb6d">waveOutClose</a>.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

