---
UID: NN:tapi3cc.ITAgentHandlerEvent
title: ITAgentHandlerEvent
author: windows-sdk-content
description: The ITAgentHandlerEvent interface contains methods that retrieve the description of agent handler events.
old-location: tapi3\itagenthandlerevent.htm
tech.root: tapi
ms.assetid: c61becce-09fd-4b12-bbc9-98df57d5f0d3
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: ITAgentHandlerEvent, ITAgentHandlerEvent interface [TAPI 2.2], ITAgentHandlerEvent interface [TAPI 2.2],described, _tapi3_itagenthandlerevent, tapi3.itagenthandlerevent, tapi3cc/ITAgentHandlerEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITAgentHandlerEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgentHandlerEvent interface


## -description


The 
<b>ITAgentHandlerEvent</b> interface contains methods that retrieve the description of agent handler events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_AGENTHANDLER</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITAgentHandlerEvent</b> interface. The methods of this interface can be used to retrieve information concerning the agent handler change that has occurred.

See 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_AGENTHANDLER</b> event to enable reception of agent handler events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/db43f4e0-f2f5-49b1-a03d-3df3de0e5611">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentHandlerEvent</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITAgentHandlerEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAgentHandlerEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7288edb3-e7df-4e31-815d-dc8fc44bb5bc">get_AgentHandler</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3362964c-15d3-497c-876b-46e8d26389c0">get_Event</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://msdn.microsoft.com/6d8340a9-dfe5-43bc-a223-d534f5b90cba">AGENTHANDLER_EVENT</a> descriptor of the event.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6d8340a9-dfe5-43bc-a223-d534f5b90cba">AGENTHANDLER_EVENT</a>



<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/6c1409c9-da73-4d21-bf56-07e9ab7b33a0">ITAgent</a>



<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

