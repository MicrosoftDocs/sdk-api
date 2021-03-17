---
UID: NF:tapi3if.ITStream.get_MediaType
title: ITStream::get_MediaType (tapi3if.h)
description: The get_MediaType method gets the stream's media type.
helpviewer_keywords: ["ITStream interface [TAPI 2.2]","get_MediaType method","ITStream.get_MediaType","ITStream::get_MediaType","_tapi3_itstream_get_mediatype","get_MediaType","get_MediaType method [TAPI 2.2]","get_MediaType method [TAPI 2.2]","ITStream interface","tapi3.itstream_get_mediatype","tapi3if/ITStream::get_MediaType"]
old-location: tapi3\itstream_get_mediatype.htm
tech.root: tapi3
ms.assetid: 871caaf3-12c4-457c-8d0f-0ee9be52a58b
ms.date: 12/05/2018
ms.keywords: ITStream interface [TAPI 2.2],get_MediaType method, ITStream.get_MediaType, ITStream::get_MediaType, _tapi3_itstream_get_mediatype, get_MediaType, get_MediaType method [TAPI 2.2], get_MediaType method [TAPI 2.2],ITStream interface, tapi3.itstream_get_mediatype, tapi3if/ITStream::get_MediaType
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
 - ITStream::get_MediaType
 - tapi3if/ITStream::get_MediaType
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
 - ITStream.get_MediaType
---

# ITStream::get_MediaType


## -description

The 
<b>get_MediaType</b> method gets the stream's 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>.

## -parameters

### -param plMediaType [out]

Pointer to media type descriptor.

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
The <i>plMediaType</i> parameter is not a valid pointer.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>