---
UID: NF:tapi3cc.ITAgent.CreateSession
title: ITAgent::CreateSession
author: windows-sdk-content
description: The CreateSession method creates a new agent session for the input ACD group and address.
old-location: tapi3\itagent_createsession.htm
old-project: tapi
ms.assetid: 68cc2ffe-3c63-4723-8652-0e28da2b17b6
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: CreateSession, CreateSession method [TAPI 2.2], CreateSession method [TAPI 2.2],ITAgent interface, ITAgent interface [TAPI 2.2],CreateSession method, ITAgent.CreateSession, ITAgent::CreateSession, _tapi3_itagent_createsession, tapi3.itagent_createsession, tapi3cc/ITAgent::CreateSession
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
 - ITAgent.CreateSession
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgent::CreateSession


## -description


The 
<b>CreateSession</b> method creates a new agent session for the input ACD group and address.


## -parameters




### -param pACDGroup [in]

Pointer to 
<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a> interface.


### -param pAddress [in]

Pointer to 
<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a> object available for receiving ACD calls.


### -param ppAgentSession [out]

Pointer to 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface for object created.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAgentSession</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Failed to open a line for the target Address.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pACDGroup</i> or <i>pAddress</i> argument is not valid.

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



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface returned by <b>ITAgent::CreateSession</b>. The application must call <b>Release</b> on the 
<b>ITAgentSession</b> interface to free resources associated with it.

Some telephone environments require a personal identification number to open a session. See 
<a href="https://msdn.microsoft.com/d901ad31-8ccc-4bca-9413-dff838a33088">CreateSessionWithPIN</a>.




## -see-also




<a href="https://msdn.microsoft.com/38b9fc57-a0af-4dfa-9058-e721138c8be9">IEnumAgentSession</a>



<a href="https://msdn.microsoft.com/73e23023-5574-4c5a-bdff-cbc7da765a65">ITACDGroup</a>



<a href="https://msdn.microsoft.com/93f2e4cf-013e-4064-88d5-69fddd458274">ITAddress</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/d901ad31-8ccc-4bca-9413-dff838a33088">ITAgent::CreateSessionWithPIN</a>



<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>
 

 

