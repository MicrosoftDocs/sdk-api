---
UID: NF:tapi3if.ITQOSEvent.get_MediaType
title: ITQOSEvent::get_MediaType (tapi3if.h)
description: The get_MediaType method gets the media type indicator.
helpviewer_keywords: ["ITQOSEvent interface [TAPI 2.2]","get_MediaType method","ITQOSEvent.get_MediaType","ITQOSEvent::get_MediaType","_tapi3_itqosevent_get_mediatype","get_MediaType","get_MediaType method [TAPI 2.2]","get_MediaType method [TAPI 2.2]","ITQOSEvent interface","tapi3.itqosevent_get_mediatype","tapi3if/ITQOSEvent::get_MediaType"]
old-location: tapi3\itqosevent_get_mediatype.htm
tech.root: tapi3
ms.assetid: 0f062eea-386d-4f25-8d51-88adbce1aefe
ms.date: 12/05/2018
ms.keywords: ITQOSEvent interface [TAPI 2.2],get_MediaType method, ITQOSEvent.get_MediaType, ITQOSEvent::get_MediaType, _tapi3_itqosevent_get_mediatype, get_MediaType, get_MediaType method [TAPI 2.2], get_MediaType method [TAPI 2.2],ITQOSEvent interface, tapi3.itqosevent_get_mediatype, tapi3if/ITQOSEvent::get_MediaType
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
 - ITQOSEvent::get_MediaType
 - tapi3if/ITQOSEvent::get_MediaType
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
 - ITQOSEvent.get_MediaType
---

# ITQOSEvent::get_MediaType


## -description

The 
<b>get_MediaType</b> method gets the 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> indicator.

## -parameters

### -param plMediaType [out]

Indicates the media type for the call on which the QOS event occurred.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent">ITQOSEvent</a>



<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>