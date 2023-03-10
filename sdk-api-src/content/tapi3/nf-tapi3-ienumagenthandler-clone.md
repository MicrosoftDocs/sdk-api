---
UID: NF:tapi3.IEnumAgentHandler.Clone
title: IEnumAgentHandler::Clone (tapi3.h)
description: The IEnumAgentHandler::Clone method (tapi3.h) creates another enumerator that contains the same enumeration state as the current one.
helpviewer_keywords: ["Clone","Clone method [TAPI 2.2]","Clone method [TAPI 2.2]","IEnumAgentHandler interface","IEnumAgentHandler interface [TAPI 2.2]","Clone method","IEnumAgentHandler.Clone","IEnumAgentHandler::Clone","_tapi3_ienumagenthandler_clone","tapi3.ienumagenthandler_clone","tapi3cc/IEnumAgentHandler::Clone"]
old-location: tapi3\ienumagenthandler_clone.htm
tech.root: tapi3
ms.assetid: a7358d0d-6d5a-4845-a212-d278a8d2b7fe
ms.date: 08/09/2022
ms.keywords: Clone, Clone method [TAPI 2.2], Clone method [TAPI 2.2],IEnumAgentHandler interface, IEnumAgentHandler interface [TAPI 2.2],Clone method, IEnumAgentHandler.Clone, IEnumAgentHandler::Clone, _tapi3_ienumagenthandler_clone, tapi3.ienumagenthandler_clone, tapi3cc/IEnumAgentHandler::Clone
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
 - IEnumAgentHandler::Clone
 - tapi3/IEnumAgentHandler::Clone
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
 - IEnumAgentHandler.Clone
---

# IEnumAgentHandler::Clone


## -description

The 
<b>Clone</b> method creates another enumerator that contains the same enumeration state as the current one.

## -parameters

### -param ppEnum [out]

Pointer to new 
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a> interface.

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
<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a> interface returned by <b>IEnumAgentHandler::Clone</b>. The application must call <b>Release</b> on the 
<b>IEnumAgentHandler</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-ienumagenthandler">IEnumAgentHandler</a>
