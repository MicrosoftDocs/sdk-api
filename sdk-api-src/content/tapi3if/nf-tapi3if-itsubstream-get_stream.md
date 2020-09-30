---
UID: NF:tapi3if.ITSubStream.get_Stream
title: ITSubStream::get_Stream (tapi3if.h)
description: The get_Stream method retrieves the pointer to the ITStream interface for the current substream.
helpviewer_keywords: ["ITSubStream interface [TAPI 2.2]","get_Stream method","ITSubStream.get_Stream","ITSubStream::get_Stream","_tapi3_itsubstream_get_stream","get_Stream","get_Stream method [TAPI 2.2]","get_Stream method [TAPI 2.2]","ITSubStream interface","tapi3.itsubstream_get_stream","tapi3if/ITSubStream::get_Stream"]
old-location: tapi3\itsubstream_get_stream.htm
tech.root: tapi3
ms.assetid: ec97e621-3789-46a4-b6b6-96639c5e7d4f
ms.date: 12/05/2018
ms.keywords: ITSubStream interface [TAPI 2.2],get_Stream method, ITSubStream.get_Stream, ITSubStream::get_Stream, _tapi3_itsubstream_get_stream, get_Stream, get_Stream method [TAPI 2.2], get_Stream method [TAPI 2.2],ITSubStream interface, tapi3.itsubstream_get_stream, tapi3if/ITSubStream::get_Stream
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
 - ITSubStream::get_Stream
 - tapi3if/ITSubStream::get_Stream
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
 - ITSubStream.get_Stream
---

# ITSubStream::get_Stream


## -description

The 
<b>get_Stream</b> method retrieves the pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface for the current substream.

## -parameters

### -param ppITStream [out]

Pointer to current 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppITStream</i> parameter is not a valid pointer.

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
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface returned by <b>ITSubStream::get_Stream</b>. The application must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>