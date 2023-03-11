---
UID: NF:tapi3.ITAgentSession.put_State
title: ITAgentSession::put_State (tapi3.h)
description: The ITAgentSession::put_State (tapi3.h) method sets the state of the agent session.
helpviewer_keywords: ["ITAgentSession interface [TAPI 2.2]","put_State method","ITAgentSession.put_State","ITAgentSession::put_State","_tapi3_itagentsession_put_state","put_State","put_State method [TAPI 2.2]","put_State method [TAPI 2.2]","ITAgentSession interface","tapi3.itagentsession_put_state","tapi3cc/ITAgentSession::put_State"]
old-location: tapi3\itagentsession_put_state.htm
tech.root: tapi3
ms.assetid: 4d35bacd-c4e4-4c31-b946-ad76ffb250ed
ms.date: 08/09/2022
ms.keywords: ITAgentSession interface [TAPI 2.2],put_State method, ITAgentSession.put_State, ITAgentSession::put_State, _tapi3_itagentsession_put_state, put_State, put_State method [TAPI 2.2], put_State method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_put_state, tapi3cc/ITAgentSession::put_State
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
 - ITAgentSession::put_State
 - tapi3/ITAgentSession::put_State
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
 - ITAgentSession.put_State
---

# ITAgentSession::put_State


## -description

The 
<b>put_State</b> method sets the state of the agent session.

## -parameters

### -param SessionState [in]

<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_session_state">AGENT_SESSION_STATE</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>SessionState</i> parameter is not a valid session state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>LINEERR_</b></dt>
</dl>
</td>
<td width="60%">
See 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentSessionState</a> for error codes returned from this TAPI 2.1 function.

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

This method wraps the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentSessionState</a> function.

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_session_state">AGENT_SESSION_STATE</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>



<a href="/windows/desktop/api/tapi3/nf-tapi3-itagentsession-get_state">get_State</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linesetagentstate">lineSetAgentSessionState</a>
