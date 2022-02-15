---
UID: NF:tapi3if.ITTAPI.Shutdown
title: ITTAPI::Shutdown (tapi3if.h)
description: The Shutdown method shuts down a TAPI session.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","Shutdown method","ITTAPI.Shutdown","ITTAPI::Shutdown","Shutdown","Shutdown method [TAPI 2.2]","Shutdown method [TAPI 2.2]","ITTAPI interface","_tapi3_ittapi_shutdown","tapi3.ittapi_shutdown","tapi3if/ITTAPI::Shutdown"]
old-location: tapi3\ittapi_shutdown.htm
tech.root: tapi3
ms.assetid: 64abb427-d41a-4670-a01c-095c678de6ff
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],Shutdown method, ITTAPI.Shutdown, ITTAPI::Shutdown, Shutdown, Shutdown method [TAPI 2.2], Shutdown method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_shutdown, tapi3.ittapi_shutdown, tapi3if/ITTAPI::Shutdown
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
 - ITTAPI::Shutdown
 - tapi3if/ITTAPI::Shutdown
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
 - ITTAPI.Shutdown
---

# ITTAPI::Shutdown


## -description

The 
<b>Shutdown</b> method shuts down a TAPI session.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
TAPI session has already been shut down.

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

One reason why 
<b>Shutdown</b> might fail is if 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-initialize">Initialize</a> was not previously called successfully.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>
