---
UID: NF:tapi3cc.ITTAPICallCenter.get_AgentHandlers
title: ITTAPICallCenter::get_AgentHandlers
author: windows-sdk-content
description: The get_AgentHandlers method creates a collection of agent handlers that are currently associated with the call center.
old-location: tapi3\ittapicallcenter_get_agenthandlers.htm
tech.root: tapi
ms.assetid: 61972ea2-d3ab-4893-8fc6-cd3c10f8584e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ITTAPICallCenter interface [TAPI 2.2],get_AgentHandlers method, ITTAPICallCenter.get_AgentHandlers, ITTAPICallCenter::get_AgentHandlers, _tapi3_ittapicallcenter_get_agenthandlers, get_AgentHandlers, get_AgentHandlers method [TAPI 2.2], get_AgentHandlers method [TAPI 2.2],ITTAPICallCenter interface, tapi3.ittapicallcenter_get_agenthandlers, tapi3cc/ITTAPICallCenter::get_AgentHandlers
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
 - ITTAPICallCenter.get_AgentHandlers
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- tapi3cc.h
: 
- ITTAPICallCenter.get_AgentHandlers
: 
---

# ITTAPICallCenter::get_AgentHandlers


## -description


The 
<b>get_AgentHandlers</b> method creates a collection of agent handlers that are currently associated with the call center. Provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="https://msdn.microsoft.com/5bd0a926-0d99-4efe-a995-28654c97c97a">EnumerateAgentHandlers</a> method.


## -parameters




### -param pVariant [out]

Pointer to a <b>VARIANT</b> containing an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface pointers.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pVariant</i> parameter is not valid.

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
The <i>pVariant</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface returned by <b>ITTAPICallCenter::get_AgentHandlers</b>. The application must call <b>Release</b> on the 
<b>ITAgentHandler</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/a318318a-769e-4619-a461-4988d90d3f1a">IEnumAgentHandler</a>



<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/871cb217-a44f-421e-9cb4-7d8771335d08">ITTAPICallCenter</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

