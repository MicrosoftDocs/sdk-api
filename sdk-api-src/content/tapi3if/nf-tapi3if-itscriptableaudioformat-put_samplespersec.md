---
UID: NF:tapi3if.ITScriptableAudioFormat.put_SamplesPerSec
title: ITScriptableAudioFormat::put_SamplesPerSec
author: windows-sdk-content
description: The put_SamplesPerSec method sets the nSamplesPerSec member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_put_samplespersec.htm
tech.root: tapi
ms.assetid: 9cf0d204-3623-4c93-9f75-39c39aa20f76
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_SamplesPerSec method, ITScriptableAudioFormat.put_SamplesPerSec, ITScriptableAudioFormat::put_SamplesPerSec, _tapi3_itscriptableaudioformat_put_samplespersec, put_SamplesPerSec, put_SamplesPerSec method [TAPI 2.2], put_SamplesPerSec method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_samplespersec, tapi3if/ITScriptableAudioFormat::put_SamplesPerSec
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
 - ITScriptableAudioFormat.put_SamplesPerSec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3if.h
: 
- ITScriptableAudioFormat.put_SamplesPerSec
: 
---

# ITScriptableAudioFormat::put_SamplesPerSec


## -description


The 
<b>put_SamplesPerSec</b> method sets the <b>nSamplesPerSec</b> member in the 
<a href="https://msdn.microsoft.com/en-us/library/Dd757713(v=VS.85).aspx">WAVEFORMATEX</a> structure.


## -parameters




### -param nNewVal [in]

New value for the <b>nSamplesPerSec</b> member in the 
<a href="https://msdn.microsoft.com/en-us/library/Dd757713(v=VS.85).aspx">WAVEFORMATEX</a> structure.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6b5d069a-044f-4bd4-b661-6100a2607107">ITScriptableAudioFormat</a>



<a href="https://msdn.microsoft.com/614e0141-76dc-40ff-ad9b-a72b95e4a46d">get_SamplesPerSec</a>
 

 

