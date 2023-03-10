---
UID: NF:tapi3.IEnumAgent.Next
title: IEnumAgent::Next (tapi3.h)
description: The IEnumAgent::Next method (tapi3.h) gets the next specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumAgent interface [TAPI 2.2]","Next method","IEnumAgent.Next","IEnumAgent::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumAgent interface","_tapi3_ienumagent_next","tapi3.ienumagent_next","tapi3cc/IEnumAgent::Next"]
old-location: tapi3\ienumagent_next.htm
tech.root: tapi3
ms.assetid: 68a7842c-557a-4da4-aa2b-e7c15a6d4f4a
ms.date: 08/09/2022
ms.keywords: IEnumAgent interface [TAPI 2.2],Next method, IEnumAgent.Next, IEnumAgent::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumAgent interface, _tapi3_ienumagent_next, tapi3.ienumagent_next, tapi3cc/IEnumAgent::Next
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
 - IEnumAgent::Next
 - tapi3/IEnumAgent::Next
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
 - IEnumAgent.Next
---

# IEnumAgent::Next


## -description

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements requested.

### -param ppElements [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> pointer.

### -param pceltFetched [out]

Pointer to number of elements actually supplied. May be <b>NULL</b> if <i>celt</i> is one.

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
Method returned <i>celt</i> number of elements.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
Number of elements remaining was less than <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppElements</i> parameter is not a valid pointer.

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

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a> interface returned by <b>IEnumAgent::Next</b>. The application must call <b>Release</b> on the 
<b>ITAgent</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagent">IEnumAgent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
