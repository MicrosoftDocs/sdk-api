---
UID: NF:tapi3.ITAgentSession.get_State
title: ITAgentSession::get_State (tapi3.h)
author: windows-sdk-content
description: The get_State method gets the current state of this session.
old-location: tapi3\itagentsession_get_state.htm
tech.root: Tapi
ms.assetid: 85a389ee-2d6c-4607-873a-8ca0c16a0fac
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],get_State method, ITAgentSession.get_State, ITAgentSession::get_State, _tapi3_itagentsession_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_state, tapi3cc/ITAgentSession::get_State
ms.topic: method
f1_keywords: ["tapi3/ITAgentSession.get_State"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentSession.get_State
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgentSession::get_State


## -description


The 
<b>get_State</b> method gets the current state of this session.


## -parameters




### -param pSessionState [out]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agent_session_state">AGENT_SESSION_STATE</a>.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSessionState</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agent_session_state">AGENT_SESSION_STATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagentsession-put_state">put_State</a>
 

 

