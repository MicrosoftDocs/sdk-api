---
UID: NN:tapi3.ITTAPICallCenter
title: ITTAPICallCenter
author: windows-driver-content
description: The ITTAPICallCenter interface provides an entry point into call center controls.
old-location: tapi3\ittapicallcenter.htm
old-project: Tapi
ms.assetid: 871cb217-a44f-421e-9cb4-7d8771335d08
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITTAPICallCenter, ITTAPICallCenter interface [TAPI 2.2], ITTAPICallCenter interface [TAPI 2.2],described, _tapi3_ittapicallcenter, tapi3.ittapicallcenter, tapi3cc/ITTAPICallCenter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: MSP_EVENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tapi3.dll
api_name:
-	ITTAPICallCenter
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITTAPICallCenter interface


## -description


The 
<b>ITTAPICallCenter</b> interface provides an entry point into call center controls. It exposes methods that allow an application to discover available agent handlers. The agent handler interface can then be used to access the other elements of a call center, such as ACD groups, agents, and queues.

The 
<b>ITTAPICallCenter</b> interface is created by calling <b>QueryInterface</b> on 
<a href="https://msdn.microsoft.com/75d641c7-dbf8-4ae2-b16b-2757e890d32b">ITTAPI</a>.

Please see 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITTAPICallCenter</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITTAPICallCenter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITTAPICallCenter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bd0a926-0d99-4efe-a995-28654c97c97a">EnumerateAgentHandlers</a>
</td>
<td align="left" width="63%">
Enumerates 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interfaces currently associated with the call center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/61972ea2-d3ab-4893-8fc6-cd3c10f8584e">get_AgentHandlers</a>
</td>
<td align="left" width="63%">
Creates a collection of 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interfaces currently associated with the call center. Provided for Automation client applications, such as those written in Visual Basic.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/55d9dd24-0902-4f6a-85f6-4ec11ce9fbaa">Call Center Interfaces</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/c4cf358f-2dc8-432a-92ed-68282ddc8a97">TAPI Object</a>
 

 

