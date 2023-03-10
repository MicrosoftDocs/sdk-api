---
UID: NF:tapi3if.ITScriptableAudioFormat.put_FormatTag
title: ITScriptableAudioFormat::put_FormatTag (tapi3if.h)
description: The put_FormatTag method sets the wFormatTag member in the WAVEFORMATEX structure.
helpviewer_keywords: ["ITScriptableAudioFormat interface [TAPI 2.2]","put_FormatTag method","ITScriptableAudioFormat.put_FormatTag","ITScriptableAudioFormat::put_FormatTag","_tapi3_itscriptableaudioformat_put_formattag","put_FormatTag","put_FormatTag method [TAPI 2.2]","put_FormatTag method [TAPI 2.2]","ITScriptableAudioFormat interface","tapi3.itscriptableaudioformat_put_formattag","tapi3if/ITScriptableAudioFormat::put_FormatTag"]
old-location: tapi3\itscriptableaudioformat_put_formattag.htm
tech.root: tapi3
ms.assetid: a57eb237-189f-4c42-a1cd-9e70f53c3c4a
ms.date: 12/05/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_FormatTag method, ITScriptableAudioFormat.put_FormatTag, ITScriptableAudioFormat::put_FormatTag, _tapi3_itscriptableaudioformat_put_formattag, put_FormatTag, put_FormatTag method [TAPI 2.2], put_FormatTag method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_formattag, tapi3if/ITScriptableAudioFormat::put_FormatTag
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITScriptableAudioFormat::put_FormatTag
 - tapi3if/ITScriptableAudioFormat::put_FormatTag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITScriptableAudioFormat.put_FormatTag
---

# ITScriptableAudioFormat::put_FormatTag


## -description

The 
<b>put_FormatTag</b> method sets the <b>wFormatTag</b> member in the 
<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

## -parameters

### -param nNewVal [in]

New value for the <b>wFormatTag</b> member in the 
<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat">ITScriptableAudioFormat</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_formattag">get_FormatTag</a>