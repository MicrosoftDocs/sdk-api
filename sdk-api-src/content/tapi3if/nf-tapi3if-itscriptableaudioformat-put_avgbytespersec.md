---
UID: NF:tapi3if.ITScriptableAudioFormat.put_AvgBytesPerSec
title: ITScriptableAudioFormat::put_AvgBytesPerSec (tapi3if.h)
description: The put_AvgBytesPerSec method sets the nAvgBytesPerSec member in the WAVEFORMATEX structure.
helpviewer_keywords: ["ITScriptableAudioFormat interface [TAPI 2.2]","put_AvgBytesPerSec method","ITScriptableAudioFormat.put_AvgBytesPerSec","ITScriptableAudioFormat::put_AvgBytesPerSec","_tapi3_itscriptableaudioformat_put_avgbytespersec","put_AvgBytesPerSec","put_AvgBytesPerSec method [TAPI 2.2]","put_AvgBytesPerSec method [TAPI 2.2]","ITScriptableAudioFormat interface","tapi3.itscriptableaudioformat_put_avgbytespersec","tapi3if/ITScriptableAudioFormat::put_AvgBytesPerSec"]
old-location: tapi3\itscriptableaudioformat_put_avgbytespersec.htm
tech.root: tapi3
ms.assetid: ca1b67b3-2dd0-47c1-9e91-ae94b6d78cc4
ms.date: 12/05/2018
ms.keywords: ITScriptableAudioFormat interface [TAPI 2.2],put_AvgBytesPerSec method, ITScriptableAudioFormat.put_AvgBytesPerSec, ITScriptableAudioFormat::put_AvgBytesPerSec, _tapi3_itscriptableaudioformat_put_avgbytespersec, put_AvgBytesPerSec, put_AvgBytesPerSec method [TAPI 2.2], put_AvgBytesPerSec method [TAPI 2.2],ITScriptableAudioFormat interface, tapi3.itscriptableaudioformat_put_avgbytespersec, tapi3if/ITScriptableAudioFormat::put_AvgBytesPerSec
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
 - ITScriptableAudioFormat::put_AvgBytesPerSec
 - tapi3if/ITScriptableAudioFormat::put_AvgBytesPerSec
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
 - ITScriptableAudioFormat.put_AvgBytesPerSec
---

# ITScriptableAudioFormat::put_AvgBytesPerSec


## -description

The 
<b>put_AvgBytesPerSec</b> method sets the <b>nAvgBytesPerSec</b> member in the 
<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure.

## -parameters

### -param nNewVal [in]

New value for the <b>nAvgBytesPerSec</b> member in the 
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



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itscriptableaudioformat-get_avgbytespersec">get_AvgBytesPerSec</a>