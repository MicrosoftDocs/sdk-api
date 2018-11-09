---
UID: NF:tapi3if.ITScriptableAudioFormat.get_BlockAlign
title: ITScriptableAudioFormat::get_BlockAlign
author: windows-sdk-content
description: The get_BlockAlign method returns the value for the nBlockAlign member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_get_blockalign.htm
tech.root: tapi
ms.assetid: 1f96d37e-af8b-4f0e-9bc0-467e3684fadb
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],get_BlockAlign method, ITScriptableAudioFormat.get_BlockAlign, ITScriptableAudioFormat::get_BlockAlign, _tapi3_itscriptableaudioformat_get_blockalign, get_BlockAlign, get_BlockAlign method [TAPI 2.2], get_BlockAlign method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_get_blockalign, tapi3if/ITScriptableAudioFormat::get_BlockAlign
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
 - ITScriptableAudioFormat.get_BlockAlign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITScriptableAudioFormat::get_BlockAlign


## -description


The 
<b>get_BlockAlign</b> method returns the value for the <b>nBlockAlign</b> member in the 
<a href="https://msdn.microsoft.com/en-us/library/Dd757713(v=VS.85).aspx">WAVEFORMATEX</a> structure.


## -parameters




### -param pVal [out]

Pointer to the value of the <b>nBlockAlign</b> member in the 
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



<a href="https://msdn.microsoft.com/bc037229-4c5f-4778-af59-02e07d03a180">put_BlockAlign</a>
 

 

