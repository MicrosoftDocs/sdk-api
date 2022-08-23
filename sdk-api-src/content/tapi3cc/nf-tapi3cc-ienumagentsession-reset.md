---
UID: NF:tapi3cc.IEnumAgentSession.Reset
title: IEnumAgentSession::Reset (tapi3cc.h)
description: The IEnumAgentSession::Reset method (tapi3cc.h) resets the enumeration sequence to the beginning.
helpviewer_keywords: ["IEnumAgentSession interface [TAPI 2.2]","Reset method","IEnumAgentSession.Reset","IEnumAgentSession::Reset","Reset","Reset method [TAPI 2.2]","Reset method [TAPI 2.2]","IEnumAgentSession interface","_tapi3_ienumagentsession_reset","tapi3.ienumagentsession_reset","tapi3cc/IEnumAgentSession::Reset"]
old-location: tapi3\ienumagentsession_reset.htm
tech.root: tapi3
ms.assetid: 38640376-0093-4fa4-9d27-b174c6df1bf4
ms.date: 08/09/2022
ms.keywords: IEnumAgentSession interface [TAPI 2.2],Reset method, IEnumAgentSession.Reset, IEnumAgentSession::Reset, Reset, Reset method [TAPI 2.2], Reset method [TAPI 2.2],IEnumAgentSession interface, _tapi3_ienumagentsession_reset, tapi3.ienumagentsession_reset, tapi3cc/IEnumAgentSession::Reset
req.header: tapi3cc.h
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
 - IEnumAgentSession::Reset
 - tapi3cc/IEnumAgentSession::Reset
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
 - IEnumAgentSession.Reset
---

# IEnumAgentSession::Reset


## -description

The 
<b>Reset</b> method resets the enumeration sequence to the beginning.



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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagentsession">IEnumAgentSession</a>
