---
UID: NF:mmeapi.waveOutPrepareHeader
title: waveOutPrepareHeader function
author: windows-sdk-content
description: The waveOutPrepareHeader function prepares a waveform-audio data block for playback.
old-location: multimedia\waveoutprepareheader.htm
tech.root: Multimedia
ms.assetid: f970c7ed-b9c5-45ce-a59b-dee02359ef82
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "_win32_waveOutPrepareHeader, mmsystem/waveOutPrepareHeader, multimedia.waveoutprepareheader, waveOutPrepareHeader, waveOutPrepareHeader function [Windows Multimedia]"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mmeapi.h
req.include-header: Mmeapi.h, Windows.h
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
 - waveOutPrepareHeader
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveOutPrepareHeader function


## -description



The <b>waveOutPrepareHeader</b> function prepares a waveform-audio data block for playback.




## -parameters




### -param hwo

Handle to the waveform-audio output device.
          


### -param pwh

Pointer to a <a href="https://msdn.microsoft.com/be70ae8e-8d8f-4261-bd0e-c6fd7feec520">WAVEHDR</a> structure that identifies the data block to be prepared.
          


### -param cbwh

Size, in bytes, of the <a href="https://msdn.microsoft.com/be70ae8e-8d8f-4261-bd0e-c6fd7feec520">WAVEHDR</a> structure.
          


## -returns



Returns <b>MMSYSERR_NOERROR</b> if successful or an error otherwise. Possible error values include the following.

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



Set the <b>lpData</b>, <b>dwBufferLength</b>, and <b>dwFlags</b> members of the <a href="https://msdn.microsoft.com/be70ae8e-8d8f-4261-bd0e-c6fd7feec520">WAVEHDR</a> structure before calling this function. Set the <b>dwFlags</b> member to zero.

The <b>dwFlags</b>, <b>dwBufferLength</b>, and <b>dwLoops</b> members of the <a href="https://msdn.microsoft.com/be70ae8e-8d8f-4261-bd0e-c6fd7feec520">WAVEHDR</a> structure can change between calls to this function and the <a href="https://msdn.microsoft.com/d687b136-8ce3-43fc-b459-b12a3fe862c8">waveOutWrite</a> function. If you change the size specified by <b>dwBufferLength</b> before the call to <b>waveOutWrite</b>, the new value must be less than the prepared value.

If the method succeeds, the <b>WHDR_PREPARED</b> flag is set in the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/be70ae8e-8d8f-4261-bd0e-c6fd7feec520">WAVEHDR</a> structure.

Preparing a header that has already been prepared has no effect, and the function returns zero.
      




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

