---
UID: NF:tapi3.ITAgentSession.get_State
title: ITAgentSession::get_State
author: windows-sdk-content
description: The get_State method gets the current state of this session.
old-location: tapi3\itagentsession_get_state.htm
old-project: Tapi
ms.assetid: 85a389ee-2d6c-4607-873a-8ca0c16a0fac
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITAgentSession interface [TAPI 2.2],get_State method, ITAgentSession.get_State, ITAgentSession::get_State, _tapi3_itagentsession_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITAgentSession interface, tapi3.itagentsession_get_state, tapi3cc/ITAgentSession::get_State
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
 - ITAgentSession.get_State
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSession::get_State


## -description


The 
<b>get_State</b> method gets the current state of this session.


## -parameters




### -param pSessionState [out]

Pointer to an 
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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSessionState</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/0c902924-e142-4ab9-9b20-661d7c2e3629">AGENT_SESSION_STATE</a>



<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>



<a href="https://msdn.microsoft.com/4d35bacd-c4e4-4c31-b946-ad76ffb250ed">put_State</a>
 

 

