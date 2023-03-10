---
UID: NF:tapi3.IEnumAgent.Clone
title: IEnumAgent::Clone (tapi3.h)
description: The IEnumAgent::Clone method (tapi3.h) creates another enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumAgent interface","IEnumAgent interface [TAPI 2.2]","Clone method","IEnumAgent.Clone","IEnumAgent::Clone","_tapi3_ienumagent_clone","tapi3.ienumagent_clone","tapi3cc/IEnumAgent::Clone"]
old-location: tapi3\ienumagent_clone.htm
tech.root: tapi3
ms.assetid: e6e23f6b-a91a-43c1-8e37-f37d7284cef6
ms.date: 08/09/2022
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumAgent interface, IEnumAgent interface [TAPI 2.2],Clone method, IEnumAgent.Clone, IEnumAgent::Clone, _tapi3_ienumagent_clone, tapi3.ienumagent_clone, tapi3cc/IEnumAgent::Clone
req.header: tapi3.h
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
 - IEnumAgent::Clone
 - tapi3/IEnumAgent::Clone
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
 - IEnumAgent.Clone
---

# IEnumAgent::Clone


## -description

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.

## -parameters

### -param ppEnum [out]

Pointer to new 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagent">IEnumAgent</a> interface.

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
The <i>ppEnum</i> parameter is not a valid pointer.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed for unknown reasons.

</td>
</tr>
</table>

## -remarks

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagent">IEnumAgent</a> interface returned by <b>IEnumAgent::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumAgent</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagent">IEnumAgent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
