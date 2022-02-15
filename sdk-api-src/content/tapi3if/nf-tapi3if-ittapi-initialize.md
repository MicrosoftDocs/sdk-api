---
UID: NF:tapi3if.ITTAPI.Initialize
title: ITTAPI::Initialize (tapi3if.h)
description: The Initialize method initializes TAPI. This method must be called before calling any other TAPI 3 method. The application must call the Shutdown method when ending a TAPI session.
helpviewer_keywords: ["ITTAPI interface [TAPI 2.2]","Initialize method","ITTAPI.Initialize","ITTAPI::Initialize","Initialize","Initialize method [TAPI 2.2]","Initialize method [TAPI 2.2]","ITTAPI interface","_tapi3_ittapi_initialize","tapi3.ittapi_initialize","tapi3if/ITTAPI::Initialize"]
old-location: tapi3\ittapi_initialize.htm
tech.root: tapi3
ms.assetid: 822ca3fe-8deb-4fe3-8b83-060eae69840c
ms.date: 12/05/2018
ms.keywords: ITTAPI interface [TAPI 2.2],Initialize method, ITTAPI.Initialize, ITTAPI::Initialize, Initialize, Initialize method [TAPI 2.2], Initialize method [TAPI 2.2],ITTAPI interface, _tapi3_ittapi_initialize, tapi3.ittapi_initialize, tapi3if/ITTAPI::Initialize
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
 - ITTAPI::Initialize
 - tapi3if/ITTAPI::Initialize
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
 - ITTAPI.Initialize
---

# ITTAPI::Initialize


## -description

The 
<b>Initialize</b> method initializes TAPI. This method must be called before calling any other TAPI 3 method. The application must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-shutdown">Shutdown</a> method when ending a TAPI session.



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
TAPI has already been initialized.

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

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapi">ITTAPI</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>
