---
UID: NF:tapi3if.ITRequestEvent.get_RequestMode
title: ITRequestEvent::get_RequestMode (tapi3if.h)
description: The get_RequestMode method gets the mode of the request.
helpviewer_keywords: ["ITRequestEvent interface [TAPI 2.2]","get_RequestMode method","ITRequestEvent.get_RequestMode","ITRequestEvent::get_RequestMode","_tapi3_itrequestevent_get_requestmode","get_RequestMode","get_RequestMode method [TAPI 2.2]","get_RequestMode method [TAPI 2.2]","ITRequestEvent interface","tapi3.itrequestevent_get_requestmode","tapi3if/ITRequestEvent::get_RequestMode"]
old-location: tapi3\itrequestevent_get_requestmode.htm
tech.root: tapi3
ms.assetid: 4c53d0ad-cb20-42f0-bd43-9b6bf18debcc
ms.date: 12/05/2018
ms.keywords: ITRequestEvent interface [TAPI 2.2],get_RequestMode method, ITRequestEvent.get_RequestMode, ITRequestEvent::get_RequestMode, _tapi3_itrequestevent_get_requestmode, get_RequestMode, get_RequestMode method [TAPI 2.2], get_RequestMode method [TAPI 2.2],ITRequestEvent interface, tapi3.itrequestevent_get_requestmode, tapi3if/ITRequestEvent::get_RequestMode
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
 - ITRequestEvent::get_RequestMode
 - tapi3if/ITRequestEvent::get_RequestMode
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
 - ITRequestEvent.get_RequestMode
---

# ITRequestEvent::get_RequestMode


## -description

The 
<b>get_RequestMode</b> method gets the mode of the request.

## -parameters

### -param plRequestMode [out]

Pointer to the request mode.

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
The <i>plRequestMode</i> is not a valid pointer.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequestevent">ITRequestEvent</a>