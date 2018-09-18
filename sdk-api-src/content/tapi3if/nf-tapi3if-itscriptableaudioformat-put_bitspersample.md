---
UID: NF:tapi3if.ITScriptableAudioFormat.put_BitsPerSample
title: ITScriptableAudioFormat::put_BitsPerSample
author: windows-sdk-content
description: The put_BitsPerSample method sets the wBitsPerSample member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_put_bitspersample.htm
tech.root: TAPI
ms.assetid: 8e1038d6-122f-40c9-a6ab-57ae583ff9bc
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_BitsPerSample method, ITScriptableAudioFormat.put_BitsPerSample, ITScriptableAudioFormat::put_BitsPerSample, _tapi3_itscriptableaudioformat_put_bitspersample, put_BitsPerSample, put_BitsPerSample method [TAPI 2.2], put_BitsPerSample method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_bitspersample, tapi3if/ITScriptableAudioFormat::put_BitsPerSample
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
 - ITScriptableAudioFormat.put_BitsPerSample
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITScriptableAudioFormat::put_BitsPerSample


## -description


The 
<b>put_BitsPerSample</b> method sets the <b>wBitsPerSample</b> member in the 
<a href="https://msdn.microsoft.com/en-us/library/Dd757713(v=VS.85).aspx">WAVEFORMATEX</a> structure.


## -parameters




### -param nNewVal [in]

New value for the <b>wBitsPerSample</b> member in the 
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



<a href="https://msdn.microsoft.com/a98a3571-89bf-4625-b495-2d080c86c4b5">get_BitsPerSample</a>
 

 

