---
UID: NF:tapi3if.IEnumSubStream.Reset
title: IEnumSubStream::Reset (tapi3if.h)
description: The Reset method resets to the beginning of the enumeration sequence. (IEnumSubStream.Reset)
helpviewer_keywords: ["IEnumSubStream interface [TAPI 2.2]","Reset method","IEnumSubStream.Reset","IEnumSubStream::Reset","Reset","Reset method [TAPI 2.2]","Reset method [TAPI 2.2]","IEnumSubStream interface","_tapi3_ienumsubstream_reset","tapi3.ienumsubstream_reset","tapi3if/IEnumSubStream::Reset"]
old-location: tapi3\ienumsubstream_reset.htm
tech.root: tapi3
ms.assetid: 72b91c81-8cfa-4879-bfcf-87fde38fcc79
ms.date: 12/05/2018
ms.keywords: IEnumSubStream interface [TAPI 2.2],Reset method, IEnumSubStream.Reset, IEnumSubStream::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumSubStream interface, _tapi3_ienumsubstream_reset, tapi3.ienumsubstream_reset, tapi3if/IEnumSubStream::Reset
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
 - IEnumSubStream::Reset
 - tapi3if/IEnumSubStream::Reset
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
 - IEnumSubStream.Reset
---

# IEnumSubStream::Reset


## -description

The 
<b>Reset</b> method resets to the beginning of the enumeration sequence.



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
Method succeeded.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumsubstream">IEnumSubStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
