---
UID: NF:tapi3if.ITMediaSupport.QueryMediaType
title: ITMediaSupport::QueryMediaType (tapi3if.h)
description: The QueryMediaType method indicates whether the service provider associated with the current address supports the media type or types indicated by lMediaType.
helpviewer_keywords: ["ITMediaSupport interface [TAPI 2.2]","QueryMediaType method","ITMediaSupport.QueryMediaType","ITMediaSupport::QueryMediaType","QueryMediaType","QueryMediaType method [TAPI 2.2]","QueryMediaType method [TAPI 2.2]","ITMediaSupport interface","_tapi3_itmediasupport_querymediatype","tapi3.itmediasupport_querymediatype","tapi3if/ITMediaSupport::QueryMediaType"]
old-location: tapi3\itmediasupport_querymediatype.htm
tech.root: tapi3
ms.assetid: 684bfd94-5bef-415b-b548-49f564ce8a83
ms.date: 12/05/2018
ms.keywords: ITMediaSupport interface [TAPI 2.2],QueryMediaType method, ITMediaSupport.QueryMediaType, ITMediaSupport::QueryMediaType, QueryMediaType, QueryMediaType method [TAPI 2.2], QueryMediaType method [TAPI 2.2],ITMediaSupport interface, _tapi3_itmediasupport_querymediatype, tapi3.itmediasupport_querymediatype, tapi3if/ITMediaSupport::QueryMediaType
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
 - ITMediaSupport::QueryMediaType
 - tapi3if/ITMediaSupport::QueryMediaType
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
 - ITMediaSupport.QueryMediaType
---

# ITMediaSupport::QueryMediaType


## -description

The 
<b>QueryMediaType</b> method indicates whether the service provider associated with the current address supports the 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> or types indicated by <i>lMediaType</i>.

## -parameters

### -param lMediaType [in]

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a> or types being queried.

### -param pfSupport [out]

Pointer to a VARIANT_BOOL indicating whether the media type is supported. If the returned value is VARIANT_TRUE, the media is supported; if it is VARIANT_FALSE, the media is not supported.

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
The <i>pfSupport</i> parameter is not a valid pointer.

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

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport">ITMediaSupport</a>