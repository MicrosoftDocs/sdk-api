---
UID: NF:tapi3if.IEnumStream.Skip
title: IEnumStream::Skip (tapi3if.h)
description: The Skip method skips over the next specified number of elements in the enumeration sequence. (IEnumStream.Skip)
helpviewer_keywords: ["IEnumStream interface [TAPI 2.2]","Skip method","IEnumStream.Skip","IEnumStream::Skip","Skip","Skip method [TAPI 2.2]","Skip method [TAPI 2.2]","IEnumStream interface","_tapi3_ienumstream_skip","tapi3.ienumstream_skip","tapi3if/IEnumStream::Skip"]
old-location: tapi3\ienumstream_skip.htm
tech.root: tapi3
ms.assetid: aa9f3a77-4e5c-43b7-9526-b621a300c2ec
ms.date: 12/05/2018
ms.keywords: IEnumStream interface [TAPI 2.2],Skip method, IEnumStream.Skip, IEnumStream::Skip, Skip, Skip method [TAPI 2.2], Skip method [TAPI 2.2],IEnumStream interface, _tapi3_ienumstream_skip, tapi3.ienumstream_skip, tapi3if/IEnumStream::Skip
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumStream::Skip
 - tapi3if/IEnumStream::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - IEnumStream.Skip
---

# IEnumStream::Skip


## -description

The 
<b>Skip</b> method skips over the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements to skip.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements skipped was not <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream">IEnumStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
