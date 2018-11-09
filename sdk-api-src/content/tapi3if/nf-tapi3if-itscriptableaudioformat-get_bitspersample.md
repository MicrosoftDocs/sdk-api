---
UID: NF:tapi3if.ITScriptableAudioFormat.get_BitsPerSample
title: ITScriptableAudioFormat::get_BitsPerSample
author: windows-sdk-content
description: The get_BitsPerSample method returns the value for the wBitsPerSample member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_get_bitspersample.htm
tech.root: tapi
ms.assetid: a98a3571-89bf-4625-b495-2d080c86c4b5
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],get_BitsPerSample method, ITScriptableAudioFormat.get_BitsPerSample, ITScriptableAudioFormat::get_BitsPerSample, _tapi3_itscriptableaudioformat_get_bitspersample, get_BitsPerSample, get_BitsPerSample method [TAPI 2.2], get_BitsPerSample method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_get_bitspersample, tapi3if/ITScriptableAudioFormat::get_BitsPerSample
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
 - ITScriptableAudioFormat.get_BitsPerSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITScriptableAudioFormat::get_BitsPerSample


## -description


The 
<b>get_BitsPerSample</b> method returns the value for the <b>wBitsPerSample</b> member in the 
<a href="_win32_waveformatex_str">WAVEFORMATEX</a> structure.


## -parameters




### -param pVal [out]

Pointer to the value of the <b>wBitsPerSample</b> member in the 
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



<a href="https://msdn.microsoft.com/8e1038d6-122f-40c9-a6ab-57ae583ff9bc">put_BitsPerSample</a>
 

 

