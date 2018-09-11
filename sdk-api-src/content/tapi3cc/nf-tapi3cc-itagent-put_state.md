---
UID: NF:tapi3cc.ITAgent.put_State
title: ITAgent::put_State
author: windows-sdk-content
description: The put_State method sets the state of an agent session.
old-location: tapi3\itagent_put_state.htm
tech.root: tapi
ms.assetid: 0f75146c-d8ce-4e9d-91bf-15dbb31b5c88
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAgent interface [TAPI 2.2],put_State method, ITAgent.put_State, ITAgent::put_State, _tapi3_itagent_put_state, put_State, put_State method [TAPI 2.2], put_State method [TAPI 2.2],ITAgent interface, tapi3.itagent_put_state, tapi3cc/ITAgent::put_State
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent.put_State
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgent::put_State


## -description


The 
<b>put_State</b> method sets the state of an agent session.


## -parameters




### -param AgentState [in]


<a href="https://msdn.microsoft.com/6d63030e-cd47-48db-ab0d-a3c4f3aac733">AGENT_STATE</a>.


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
<a href="https://msdn.microsoft.com/f7da697a-658e-4f0d-8e6c-539fd8fb1935">lineSetAgentStateEx</a> function.




## -see-also




<a href="https://msdn.microsoft.com/6d63030e-cd47-48db-ab0d-a3c4f3aac733">AGENT_STATE</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/6690a62b-65a1-4892-aeee-4a6652939d5f">get_State</a>
 

 

