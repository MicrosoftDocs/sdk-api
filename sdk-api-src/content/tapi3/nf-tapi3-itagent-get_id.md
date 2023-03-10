---
UID: NF:tapi3.ITAgent.get_ID
title: ITAgent::get_ID (tapi3.h)
description: The ITAgent::get_ID method (tapi3.h) gets an agent's ID.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_ID method","ITAgent.get_ID","ITAgent::get_ID","_tapi3_itagent_get_id","get_ID","get_ID method [TAPI 2.2]","get_ID method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_id","tapi3cc/ITAgent::get_ID"]
old-location: tapi3\itagent_get_id.htm
tech.root: tapi3
ms.assetid: e5045dd7-5a12-415e-b68a-f483f77f4887
ms.date: 08/09/2022
ms.keywords: ITAgent interface [TAPI 2.2],get_ID method, ITAgent.get_ID, ITAgent::get_ID, _tapi3_itagent_get_id, get_ID, get_ID method [TAPI 2.2], get_ID method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_id, tapi3cc/ITAgent::get_ID
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
 - ITAgent::get_ID
 - tapi3/ITAgent::get_ID
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
 - ITAgent.get_ID
---

# ITAgent::get_ID


## -description

The 
<b>get_ID</b> method gets an agent's ID.

## -parameters

### -param ppID [out]

Pointer to <b>BSTR</b> containing agent ID.

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
<dt><b>TAPI_E_CALLCENTER_NO_AGENT_ID</b></dt>
</dl>
</td>
<td width="60%">
ITAgent was not created using 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagentwithid">ITAgentHandler::CreateAgentWithID</a>, but with 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-createagent">ITAgentHandler::CreateAgent</a>. No ID exists.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppID</i> parameter is not a valid pointer.

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

This method is provided for interfacing with legacy switch solutions.

The application must free the memory allocated for the <i>ppID</i> parameter through 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> when the variable is no longer needed.

## -see-also

<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>
