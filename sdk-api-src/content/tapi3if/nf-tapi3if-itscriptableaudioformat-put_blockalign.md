---
UID: NF:tapi3if.ITScriptableAudioFormat.put_BlockAlign
title: ITScriptableAudioFormat::put_BlockAlign (tapi3if.h)
author: windows-sdk-content
description: The put_BlockAlign method sets the nBlockAlign member in the WAVEFORMATEX structure.
old-location: tapi3\itscriptableaudioformat_put_blockalign.htm
tech.root: Tapi
ms.assetid: bc037229-4c5f-4778-af59-02e07d03a180
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_BlockAlign method, ITScriptableAudioFormat.put_BlockAlign, ITScriptableAudioFormat::put_BlockAlign, _tapi3_itscriptableaudioformat_put_blockalign, put_BlockAlign, put_BlockAlign method [TAPI 2.2], put_BlockAlign method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_blockalign, tapi3if/ITScriptableAudioFormat::put_BlockAlign
ms.topic: method
f1_keywords: 
 - "tapi3if/ITScriptableAudioFormat.put_BlockAlign"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITScriptableAudioFormat::put_BlockAlign


## -description


The 
<b>put_BlockAlign</b> method sets the <b>nBlockAlign</b> member in the 
<a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.


## -parameters




### -param nNewVal [in]

New value for the <b>nBlockAlign</b> member in the 
<a href="https://docs.microsoft.com/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.


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




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_blockalign">get_BlockAlign</a>
 

 

