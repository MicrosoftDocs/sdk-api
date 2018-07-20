---
UID: NF:tapi3.ITAgent.get_AgentSessions
title: ITAgent::get_AgentSessions
author: windows-sdk-content
description: The get_AgentSessions method creates a collection of current agent sessions. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateAgentSessions method.
old-location: tapi3\itagent_get_agentsessions.htm
old-project: tapi
ms.assetid: 25503eae-ebee-4b57-ab5c-b3f152de9a96
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITAgent interface [TAPI 2.2],get_AgentSessions method, ITAgent.get_AgentSessions, ITAgent::get_AgentSessions, _tapi3_itagent_get_agentsessions, get_AgentSessions, get_AgentSessions method [TAPI 2.2], get_AgentSessions method [TAPI 2.2],ITAgent interface, tapi3.itagent_get_agentsessions, tapi3cc/ITAgent::get_AgentSessions
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
 - ITAgent.get_AgentSessions
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgent::get_AgentSessions


## -description


The 
<b>get_AgentSessions</b> method creates a collection of current agent sessions. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/6b639a41-c866-49ad-bc33-1215da7c8a19">EnumerateAgentSessions</a> method.


## -parameters




### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface pointers (agent session objects).


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
The <i>pVariant</i> parameter is not a valid pointer.

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
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface returned by <b>ITAgent::get_AgentSessions</b>. The application must call <b>Release</b> on the 
<b>ITAgentSession</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/6b639a41-c866-49ad-bc33-1215da7c8a19">EnumerateAgentSessions</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<b>ITAgentSession</b>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>
 

 

