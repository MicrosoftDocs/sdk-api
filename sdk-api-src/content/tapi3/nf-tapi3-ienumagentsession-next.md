---
UID: NF:tapi3.IEnumAgentSession.Next
title: IEnumAgentSession::Next (tapi3.h)
description: The IEnumAgentSession::Next method (tapi3.h) gets the next specified number of elements in the enumeration sequence.
helpviewer_keywords: ["IEnumAgentSession interface [TAPI 2.2]","Next method","IEnumAgentSession.Next","IEnumAgentSession::Next","Next","Next method [TAPI 2.2]","Next method [TAPI 2.2]","IEnumAgentSession interface","_tapi3_ienumagentsession_next","tapi3.ienumagentsession_next","tapi3cc/IEnumAgentSession::Next"]
old-location: tapi3\ienumagentsession_next.htm
tech.root: tapi3
ms.assetid: 5ac647a0-7f1a-4f6a-ad01-dba019f9bf56
ms.date: 08/09/2022
ms.keywords: IEnumAgentSession interface [TAPI 2.2],Next method, IEnumAgentSession.Next, IEnumAgentSession::Next, Next, Next method [TAPI 2.2], Next method [TAPI 2.2],IEnumAgentSession interface, _tapi3_ienumagentsession_next, tapi3.ienumagentsession_next, tapi3cc/IEnumAgentSession::Next
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
 - IEnumAgentSession::Next
 - tapi3/IEnumAgentSession::Next
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
 - IEnumAgentSession.Next
---

# IEnumAgentSession::Next


## -description

The 
<b>Next</b> method gets the next specified number of elements in the enumeration sequence.

## -parameters

### -param celt [in]

Number of elements requested.

### -param ppElements [out]

Pointer to 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface.

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
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a> interface returned by <b>IEnumAgentSession::Next</b>. The application must call <b>Release</b> on the 
<b>ITAgentSession</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagentsession">IEnumAgentSession</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>
