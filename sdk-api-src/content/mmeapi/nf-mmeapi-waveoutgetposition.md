---
UID: NF:mmeapi.waveOutGetPosition
title: waveOutGetPosition function
author: windows-sdk-content
description: The waveOutGetPosition function retrieves the current playback position of the given waveform-audio output device.
old-location: multimedia\waveoutgetposition.htm
tech.root: Multimedia
ms.assetid: 66279da3-0ed7-489b-a465-88e781a8443d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_waveOutGetPosition, mmeapi/waveOutGetPosition, multimedia.waveoutgetposition, waveOutGetPosition, waveOutGetPosition function [Windows Multimedia]"
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
 - waveOutGetPosition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveOutGetPosition function


## -description



The <b>waveOutGetPosition</b> function retrieves the current playback position of the given waveform-audio output device.




## -parameters




### -param hwo

Handle to the waveform-audio output device.


### -param pmmt

Pointer to an <a href="https://msdn.microsoft.com/94bb7235-2477-4923-add8-f0c8ac8195c2">MMTIME</a> structure.


### -param cbmmt

Size, in bytes, of the <b>MMTIME</b> structure.


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



Before calling this function, set the <b>wType</b> member of the <b>MMTIME</b> structure to indicate the time format you want. After calling this function, check <b>wType</b> to determine whether the time format is supported. If the format is not supported, <b>wType</b> will specify an alternative format.

The position is set to zero when the device is opened or reset.




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

