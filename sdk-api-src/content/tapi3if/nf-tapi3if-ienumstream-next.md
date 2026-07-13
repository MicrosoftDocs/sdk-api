---
UID: NF:tapi3if.IEnumStream.Next
title: IEnumStream::Next (tapi3if.h)
description: The Next method gets the next specified number of elements in the enumeration sequence. (IEnumStream.Next)
helpviewer_keywords: ["IEnumStream interface [TAPI 2.2]","Next method","IEnumStream.Next","IEnumStream::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumStream interface","_tapi3_ienumstream_next","tapi3.ienumstream_next","tapi3if/IEnumStream::Next"]
old-location: tapi3\ienumstream_next.htm
tech.root: tapi3
ms.assetid: 96399092-88fa-4b3c-aede-ee61c7c0320a
ms.date: 12/05/2018
ms.keywords: IEnumStream interface [TAPI 2.2],Next method, IEnumStream.Next, IEnumStream::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumStream interface, _tapi3_ienumstream_next, tapi3.ienumstream_next, tapi3if/IEnumStream::Next
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
 - IEnumStream::Next
 - tapi3if/IEnumStream::Next
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
 - IEnumStream.Next
---

# IEnumStream::Next


## -description

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements requested.

### -param ppElements [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> pointers returned.

### -param pceltFetched [out]

Pointer to number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.

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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

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

## -remarks

TAPI calls the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface returned by <b>IEnumStream::Next</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<b>ITStream</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream">IEnumStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
