---
UID: NF:tapi3if.ITScriptableAudioFormat.get_SamplesPerSec
title: ITScriptableAudioFormat::get_SamplesPerSec
author: windows-sdk-content
description: The get_SamplesPerSec method returns the value for the nSamplesPerSec member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_get_samplespersec.htm
tech.root: tapi
ms.assetid: 614e0141-76dc-40ff-ad9b-a72b95e4a46d
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],get_SamplesPerSec method, ITScriptableAudioFormat.get_SamplesPerSec, ITScriptableAudioFormat::get_SamplesPerSec, _tapi3_itscriptableaudioformat_get_samplespersec, get_SamplesPerSec, get_SamplesPerSec method [TAPI 2.2], get_SamplesPerSec method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_get_samplespersec, tapi3if/ITScriptableAudioFormat::get_SamplesPerSec
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITScriptableAudioFormat.get_SamplesPerSec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITScriptableAudioFormat::get_SamplesPerSec


## -description


The 
<b>get_SamplesPerSec</b> method returns the value for the <b>nSamplesPerSec</b> member in the 
<a href="_win32_waveformatex_str">WAVEFORMATEX</a> structure.


## -parameters




### -param pVal [out]

Pointer to the value of the <b>nSamplesPerSec</b> member in the 
<a href="_win32_waveformatex_str">WAVEFORMATEX</a> structure.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVal</i> argument is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6b5d069a-044f-4bd4-b661-6100a2607107">ITScriptableAudioFormat</a>



<a href="https://msdn.microsoft.com/9cf0d204-3623-4c93-9f75-39c39aa20f76">put_SamplesPerSec</a>
 

 

