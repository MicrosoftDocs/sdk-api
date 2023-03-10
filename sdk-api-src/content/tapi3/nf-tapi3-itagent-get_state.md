---
UID: NF:tapi3.ITAgent.get_State
title: ITAgent::get_State (tapi3.h)
description: The get_State method (tapi3.h) gets the state of an agent session.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","get_State method","ITAgent.get_State","ITAgent::get_State","_tapi3_itagent_get_state","get_State","get_State method [TAPI 2.2]","get_State method [TAPI 2.2]","ITAgent interface","tapi3.itagent_get_state","tapi3cc/ITAgent::get_State"]
old-location: tapi3\itagent_get_state.htm
tech.root: tapi3
ms.assetid: 6690a62b-65a1-4892-aeee-4a6652939d5f
ms.date: 08/09/2022
ms.keywords: ITAgent interface [TAPI 2.2],get_State method, ITAgent.get_State, ITAgent::get_State, _tapi3_itagent_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_state, tapi3cc/ITAgent::get_State
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
 - ITAgent::get_State
 - tapi3/ITAgent::get_State
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
 - ITAgent.get_State
---

# ITAgent::get_State


## -description

The 
<b>get_State</b> method gets the state of an agent session.

## -parameters

### -param pAgentState [out]

Pointer to an 
<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_state">AGENT_STATE</a>.

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
The <i>pAgentState</i> parameter is not a valid pointer.

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

<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_state">AGENT_STATE</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-put_state">put_State</a>
