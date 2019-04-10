---
UID: NF:mmeapi.waveInStart
title: waveInStart function (mmeapi.h)
author: windows-sdk-content
description: The waveInStart function starts input on the given waveform-audio input device.
old-location: multimedia\waveinstart.htm
tech.root: Multimedia
ms.assetid: f55625f4-1503-48ea-a654-eb87d1db3043
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "_win32_waveInStart, mmeapi/waveInStart, multimedia.waveinstart, waveInStart, waveInStart function [Windows Multimedia]"
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
 - waveInStart
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveInStart function


## -description



The <b>waveInStart</b> function starts input on the given waveform-audio input device.




## -parameters




### -param hwi

Handle to the waveform-audio input device.


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



Buffers are returned to the application when full or when the <b>waveInReset</b> function is called (the <b>dwBytesRecorded</b> member in the header will contain the length of data). If there are no buffers in the queue, the data is thrown away without notifying the application, and input continues.

Calling this function when input is already started has no effect, and the function returns zero.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

