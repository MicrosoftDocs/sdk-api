---
UID: NF:tapi3if.ITTerminal.get_MediaType
title: ITTerminal::get_MediaType (tapi3if.h)
description: The get_MediaType method determines the media that this terminal supports.
helpviewer_keywords: ["ITTerminal interface [TAPI 2.2]","get_MediaType method","ITTerminal.get_MediaType","ITTerminal::get_MediaType","_tapi3_itterminal_get_mediatype","get_MediaType","get_MediaType method [TAPI 2.2]","get_MediaType method [TAPI 2.2]","ITTerminal interface","tapi3.itterminal_get_mediatype","tapi3if/ITTerminal::get_MediaType"]
old-location: tapi3\itterminal_get_mediatype.htm
tech.root: tapi3
ms.assetid: 8c2006ad-d2f9-4e21-b0ae-583ec3ff82f4
ms.date: 12/05/2018
ms.keywords: ITTerminal interface [TAPI 2.2],get_MediaType method, ITTerminal.get_MediaType, ITTerminal::get_MediaType, _tapi3_itterminal_get_mediatype, get_MediaType, get_MediaType method [TAPI 2.2], get_MediaType method [TAPI 2.2],ITTerminal interface, tapi3.itterminal_get_mediatype, tapi3if/ITTerminal::get_MediaType
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
 - ITTerminal::get_MediaType
 - tapi3if/ITTerminal::get_MediaType
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
 - ITTerminal.get_MediaType
---

# ITTerminal::get_MediaType


## -description

The 
<b>get_MediaType</b> method determines the media that this terminal supports.

## -parameters

### -param plMediaType [out]

Pointer to 
<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>