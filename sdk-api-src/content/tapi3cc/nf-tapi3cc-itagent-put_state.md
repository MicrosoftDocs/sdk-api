---
UID: NF:tapi3cc.ITAgent.put_State
title: ITAgent::put_State (tapi3cc.h)
description: The ITAgent::put_State method (tapi3cc.h) sets the state of an agent session.
helpviewer_keywords: ["ITAgent interface [TAPI 2.2]","put_State method","ITAgent.put_State","ITAgent::put_State","_tapi3_itagent_put_state","put_State","put_State method [TAPI 2.2]","put_State method [TAPI 2.2]","ITAgent interface","tapi3.itagent_put_state","tapi3cc/ITAgent::put_State"]
old-location: tapi3\itagent_put_state.htm
tech.root: tapi3
ms.assetid: 0f75146c-d8ce-4e9d-91bf-15dbb31b5c88
ms.date: 08/10/2022
ms.keywords: ITAgent interface [TAPI 2.2],put_State method, ITAgent.put_State, ITAgent::put_State, _tapi3_itagent_put_state, put_State, put_State method [TAPI 2.2], put_State method [TAPI 2.2],ITAgent interface, tapi3.itagent_put_state, tapi3cc/ITAgent::put_State
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
 - ITAgent::put_State
 - tapi3cc/ITAgent::put_State
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
 - ITAgent.put_State
---

# ITAgent::put_State


## -description

The 
<b>put_State</b> method sets the state of an agent session.

## -parameters

### -param AgentState [in]

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Agent session state is incorrect.

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
<dt><b>TAPI_E_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The operation failed because the TAPI 3 DLL timed it out. The timeout interval is two minutes.

</td>
</tr>
</table>

## -remarks

The <b>ITAgent::put_State</b> method is a COM wrapper for the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstateex">lineSetAgentStateEx</a> function.

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_state">AGENT_STATE</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagent-get_state">get_State</a>
