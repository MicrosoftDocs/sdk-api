---
UID: NF:tapi3.ITAgent.EnumerateAgentSessions
title: ITAgent::EnumerateAgentSessions
author: windows-sdk-content
description: The EnumerateAgentSessions method enumerates the current agent sessions. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_AgentSessions method.
old-location: tapi3\itagent_enumerateagentsessions.htm
tech.root: tapi
ms.assetid: 6b639a41-c866-49ad-bc33-1215da7c8a19
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: EnumerateAgentSessions, EnumerateAgentSessions method [TAPI 2.2], EnumerateAgentSessions method [TAPI 2.2],ITAgent interface, ITAgent interface [TAPI 2.2],EnumerateAgentSessions method, ITAgent.EnumerateAgentSessions, ITAgent::EnumerateAgentSessions, _tapi3_itagent_enumerateagentsessions, tapi3.itagent_enumerateagentsessions, tapi3cc/ITAgent::EnumerateAgentSessions
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITAgent.EnumerateAgentSessions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgent::EnumerateAgentSessions


## -description


The 
<b>EnumerateAgentSessions</b> method enumerates the current agent sessions. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="https://msdn.microsoft.com/25503eae-ebee-4b57-ab5c-b3f152de9a96">get_AgentSessions</a> method.


## -parameters




### -param ppEnumAgentSession [out]

Pointer to an 
<a href="https://msdn.microsoft.com/38b9fc57-a0af-4dfa-9058-e721138c8be9">IEnumAgentSession</a> agent session enumerator.


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
The <b>ppEnumAgentSession</b> parameter is not a valid pointer.

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



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/38b9fc57-a0af-4dfa-9058-e721138c8be9">IEnumAgentSession</a> interface returned by <b>ITAgent::EnumerateAgentSessions</b>. The application must call <b>Release</b> on the 
<b>IEnumAgentSession</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/38b9fc57-a0af-4dfa-9058-e721138c8be9">IEnumAgentSession</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/68cc2ffe-3c63-4723-8652-0e28da2b17b6">ITAgent::CreateSession</a>



<a href="https://msdn.microsoft.com/d901ad31-8ccc-4bca-9413-dff838a33088">ITAgent::CreateSessionWithPIN</a>



<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>



<a href="https://msdn.microsoft.com/25503eae-ebee-4b57-ab5c-b3f152de9a96">get_AgentSessions</a>
 

 

