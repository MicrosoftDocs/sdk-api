---
UID: NF:tapi3cc.ITAgent.get_State
title: ITAgent::get_State
author: windows-sdk-content
description: The get_State method gets the state of an agent session.
old-location: tapi3\itagent_get_state.htm
tech.root: tapi
ms.assetid: 6690a62b-65a1-4892-aeee-4a6652939d5f
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_State method, ITAgent.get_State, ITAgent::get_State, _tapi3_itagent_get_state, get_State, get_State method [TAPI 2.2], get_State method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_state, tapi3cc/ITAgent::get_State
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
 - ITAgent.get_State
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgent::get_State


## -description


The 
<b>get_State</b> method gets the state of an agent session.


## -parameters




### -param pAgentState [out]

Pointer to an 
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




<a href="https://msdn.microsoft.com/6d63030e-cd47-48db-ab0d-a3c4f3aac733">AGENT_STATE</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/0f75146c-d8ce-4e9d-91bf-15dbb31b5c88">put_State</a>
 

 

