---
UID: NF:tapi3if.ITScriptableAudioFormat.get_FormatTag
title: ITScriptableAudioFormat::get_FormatTag
author: windows-sdk-content
description: The get_FormatTag method returns the value for the wFormatTag member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_get_formattag.htm
old-project: tapi
ms.assetid: 073e4800-d84a-4f12-81ce-eba4a4e139fc
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],get_FormatTag method, ITScriptableAudioFormat.get_FormatTag, ITScriptableAudioFormat::get_FormatTag, _tapi3_itscriptableaudioformat_get_formattag, get_FormatTag, get_FormatTag method [TAPI 2.2], get_FormatTag method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_get_formattag, tapi3if/ITScriptableAudioFormat::get_FormatTag
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITScriptableAudioFormat.get_FormatTag
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITScriptableAudioFormat::get_FormatTag


## -description


The 
<b>get_FormatTag</b> method returns the value for the <b>wFormatTag</b> member in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure.


## -parameters




### -param pVal [out]

Pointer to the value of the <b>wFormatTag</b> member in the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure.


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



<a href="https://msdn.microsoft.com/a57eb237-189f-4c42-a1cd-9e70f53c3c4a">put_FormatTag</a>
 

 

