---
UID: NF:mmeapi.waveInGetID
title: waveInGetID function (mmeapi.h)
author: windows-sdk-content
description: The waveInGetID function gets the device identifier for the given waveform-audio input device.
old-location: multimedia\waveingetid.htm
tech.root: Multimedia
ms.assetid: 57ca501d-3f76-4ccc-94dc-b4b5c40932e0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "_win32_waveInGetID, mmeapi/waveInGetID, multimedia.waveingetid, waveInGetID, waveInGetID function [Windows Multimedia]"
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
 - waveInGetID
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# waveInGetID function


## -description



The <b>waveInGetID</b> function gets the device identifier for the given waveform-audio input device.



This function is supported for backward compatibility. New applications can cast a handle of the device rather than retrieving the device identifier.


## -parameters




### -param hwi

Handle to the waveform-audio input device.


### -param puDeviceID

Pointer to a variable to be filled with the device identifier.


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
The <i>hwi</i> parameter specifies an invalid handle.

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
 




## -see-also




<a href="https://msdn.microsoft.com/3188355c-65be-4372-8e87-e7f755982592">Waveform Audio</a>



<a href="https://msdn.microsoft.com/6c8aaa54-0477-484f-91e1-d2152aa9c185">Waveform Functions</a>
 

 

