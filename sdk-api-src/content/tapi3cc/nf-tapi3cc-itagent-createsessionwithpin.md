---
UID: NF:tapi3cc.ITAgent.CreateSessionWithPIN
title: ITAgent::CreateSessionWithPIN
author: windows-sdk-content
description: The CreateSessionWithPIN method creates a new agent session for the input ACD group and address, with Personal Identification Number (PIN).
old-location: tapi3\itagent_createsessionwithpin.htm
old-project: Tapi
ms.assetid: d901ad31-8ccc-4bca-9413-dff838a33088
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: CreateSessionWithPIN, CreateSessionWithPIN method [TAPI 2.2], CreateSessionWithPIN method [TAPI 2.2],ITAgent interface, ITAgent interface [TAPI 2.2],CreateSessionWithPIN method, ITAgent.CreateSessionWithPIN, ITAgent::CreateSessionWithPIN, _tapi3_itagent_createsessionwithpin, tapi3.itagent_createsessionwithpin, tapi3cc/ITAgent::CreateSessionWithPIN
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AGENT_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgent.CreateSessionWithPIN
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgent::CreateSessionWithPIN


## -description


The 
<b>CreateSessionWithPIN</b> method creates a new agent session for the input ACD group and address, with Personal Identification Number (PIN).


## -parameters




### -param pACDGroup [in]

Pointer to 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface.


### -param pAddress [in]

Pointer to 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> interface for object available for receiving ACD calls.


### -param pPIN [in]

Pointer to a <b>BSTR</b> representation of agent's PIN.


### -param ppAgentSession [out]

Pointer to session created.


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
<dt><b>TAPI_E_CALLCENTER_NO_AGENT_ID</b></dt>
</dl>
</td>
<td width="60%">
Agent not created by 
<a href="https://msdn.microsoft.com/95c70e48-b990-47c7-a8b8-5fa3a84ec5ba">CreateAgentWithID</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pPIN</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pPIN</i> or <i>ppAgentSession</i> parameter is not a valid pointer.

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



The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for <i>pPIN</i> and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface returned by <b>ITAgent::CreateSessionWithPIN</b>. The application must call <b>Release</b> on the 
<b>ITAgentSession</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/68cc2ffe-3c63-4723-8652-0e28da2b17b6">ITAgent::CreateSession</a>



<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>
 

 

