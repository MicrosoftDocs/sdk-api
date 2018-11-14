---
UID: NF:tapi3.ITAgentHandlerEvent.get_AgentHandler
title: ITAgentHandlerEvent::get_AgentHandler
author: windows-sdk-content
description: The get_AgentHandler method gets the ITAgentHandler interface pointer.
old-location: tapi3\itagenthandlerevent_get_agenthandler.htm
tech.root: tapi
ms.assetid: 7288edb3-e7df-4e31-815d-dc8fc44bb5bc
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITAgentHandlerEvent interface [TAPI 2.2],get_AgentHandler method, ITAgentHandlerEvent.get_AgentHandler, ITAgentHandlerEvent::get_AgentHandler, _tapi3_itagenthandlerevent_get_agenthandler, get_AgentHandler, get_AgentHandler method [TAPI 2.2], get_AgentHandler method [TAPI 2.2],ITAgentHandlerEvent interface, tapi3.itagenthandlerevent_get_agenthandler, tapi3cc/ITAgentHandlerEvent::get_AgentHandler
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
 - ITAgentHandlerEvent.get_AgentHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3.h
: 
- ITAgentHandlerEvent.get_AgentHandler
: 
---

# ITAgentHandlerEvent::get_AgentHandler


## -description


The 
<b>get_AgentHandler</b> method gets the 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface pointer.


## -parameters




### -param ppAgentHandler [out]

Pointer to the 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface on which the event occurred.


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
The <i>ppAgentHandler</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface returned by <b>ITAgentHandlerEvent::get_AgentHandler</b>. The application must call <b>Release</b> on the 
<b>ITAgentHandler</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>



<a href="https://msdn.microsoft.com/c61becce-09fd-4b12-bbc9-98df57d5f0d3">ITAgentHandlerEvent</a>
 

 

