---
UID: NF:tapi3.ITAgentSession.put_State
title: ITAgentSession::put_State
author: windows-sdk-content
description: The put_State method sets the state of the agent session.
old-location: tapi3\itagentsession_put_state.htm
old-project: tapi
ms.assetid: 4d35bacd-c4e4-4c31-b946-ad76ffb250ed
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],put_State method, ITAgentSession.put_State, ITAgentSession::put_State, _tapi3_itagentsession_put_state, put_State, put_State method [TAPI 2.2], put_State method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_put_state, tapi3cc/ITAgentSession::put_State
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSP_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentSession.put_State
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSession::put_State


## -description


The 
<b>put_State</b> method sets the state of the agent session.


## -parameters




### -param SessionState [in]


<a href="https://msdn.microsoft.com/0c902924-e142-4ab9-9b20-661d7c2e3629">AGENT_SESSION_STATE</a>.


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
<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentSessionState</a> for error codes returned from this TAPI 2.1 function.

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
<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentSessionState</a> function.




## -see-also




<a href="https://msdn.microsoft.com/0c902924-e142-4ab9-9b20-661d7c2e3629">AGENT_SESSION_STATE</a>



<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>



<a href="https://msdn.microsoft.com/85a389ee-2d6c-4607-873a-8ca0c16a0fac">get_State</a>



<a href="https://msdn.microsoft.com/985798fd-54b1-4674-a1fe-b72c56c5176b">lineSetAgentSessionState</a>
 

 

