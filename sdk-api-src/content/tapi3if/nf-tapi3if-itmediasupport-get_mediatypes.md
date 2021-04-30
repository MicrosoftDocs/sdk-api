---
UID: NF:tapi3if.ITMediaSupport.get_MediaTypes
title: ITMediaSupport::get_MediaTypes (tapi3if.h)
description: The get_MediaTypes method gets the media type or types supported on the current address.
helpviewer_keywords: ["ITMediaSupport interface [TAPI 2.2]","get_MediaTypes method","ITMediaSupport.get_MediaTypes","ITMediaSupport::get_MediaTypes","_tapi3_itmediasupport_get_mediatypes","get_MediaTypes","get_MediaTypes method [TAPI 2.2]","get_MediaTypes method [TAPI 2.2]","ITMediaSupport interface","tapi3.itmediasupport_get_mediatypes","tapi3if/ITMediaSupport::get_MediaTypes"]
old-location: tapi3\itmediasupport_get_mediatypes.htm
tech.root: tapi3
ms.assetid: 8fc3d82e-6d6f-4442-9232-87f8d7605870
ms.date: 12/05/2018
ms.keywords: ITMediaSupport interface [TAPI 2.2],get_MediaTypes method, ITMediaSupport.get_MediaTypes, ITMediaSupport::get_MediaTypes, _tapi3_itmediasupport_get_mediatypes, get_MediaTypes, get_MediaTypes method [TAPI 2.2], get_MediaTypes method [TAPI 2.2],ITMediaSupport interface, tapi3.itmediasupport_get_mediatypes, tapi3if/ITMediaSupport::get_MediaTypes
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
 - ITMediaSupport::get_MediaTypes
 - tapi3if/ITMediaSupport::get_MediaTypes
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
 - ITMediaSupport.get_MediaTypes
---

# ITMediaSupport::get_MediaTypes


## -description

The 
<b>get_MediaTypes</b> method gets the 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a> or types supported on the current address.

## -parameters

### -param plMediaTypes [out]

Pointer to bitmask of ORed of 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>.

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
The <i>plMediaTypes</i> parameter is not a valid pointer.

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