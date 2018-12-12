---
UID: NF:tapi3if.ITScriptableAudioFormat.put_BlockAlign
title: ITScriptableAudioFormat::put_BlockAlign
author: windows-sdk-content
description: The put_BlockAlign method sets the nBlockAlign member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_put_blockalign.htm
tech.root: tapi
ms.assetid: bc037229-4c5f-4778-af59-02e07d03a180
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_BlockAlign method, ITScriptableAudioFormat.put_BlockAlign, ITScriptableAudioFormat::put_BlockAlign, _tapi3_itscriptableaudioformat_put_blockalign, put_BlockAlign, put_BlockAlign method [TAPI 2.2], put_BlockAlign method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_blockalign, tapi3if/ITScriptableAudioFormat::put_BlockAlign
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
 - ITScriptableAudioFormat.put_BlockAlign
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITScriptableAudioFormat::put_BlockAlign


## -description


The 
<b>put_BlockAlign</b> method sets the <b>nBlockAlign</b> member in the 
<a href="_win32_waveformatex_str">WAVEFORMATEX</a> structure.


## -parameters




### -param nNewVal [in]

New value for the <b>nBlockAlign</b> member in the 
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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6b5d069a-044f-4bd4-b661-6100a2607107">ITScriptableAudioFormat</a>



<a href="https://msdn.microsoft.com/1f96d37e-af8b-4f0e-9bc0-467e3684fadb">get_BlockAlign</a>
 

 

