---
UID: NF:tapi3if.ITScriptableAudioFormat.put_FormatTag
title: ITScriptableAudioFormat::put_FormatTag
author: windows-sdk-content
description: The put_FormatTag method sets the wFormatTag member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_put_formattag.htm
tech.root: tapi
ms.assetid: a57eb237-189f-4c42-a1cd-9e70f53c3c4a
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_FormatTag method, ITScriptableAudioFormat.put_FormatTag, ITScriptableAudioFormat::put_FormatTag, _tapi3_itscriptableaudioformat_put_formattag, put_FormatTag, put_FormatTag method [TAPI 2.2], put_FormatTag method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_formattag, tapi3if/ITScriptableAudioFormat::put_FormatTag
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
 - ITScriptableAudioFormat.put_FormatTag
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITScriptableAudioFormat::put_FormatTag


## -description


The 
<b>put_FormatTag</b> method sets the <b>wFormatTag</b> member in the 
<a href="https://msdn.microsoft.com/en-us/library/Dd757713(v=VS.85).aspx">WAVEFORMATEX</a> structure.


## -parameters




### -param nNewVal [in]

New value for the <b>wFormatTag</b> member in the 
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



<a href="https://msdn.microsoft.com/073e4800-d84a-4f12-81ce-eba4a4e139fc">get_FormatTag</a>
 

 

