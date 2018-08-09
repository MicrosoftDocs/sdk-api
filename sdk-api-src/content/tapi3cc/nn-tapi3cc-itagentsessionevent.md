---
UID: NN:tapi3cc.ITAgentSessionEvent
title: ITAgentSessionEvent
author: windows-sdk-content
description: The ITAgentSessionEvent interface contains methods that retrieve the description of agent session events.
old-location: tapi3\itagentsessionevent.htm
old-project: tapi
ms.assetid: 70d37d06-b1a6-4f7e-bfe5-731d1b4cd66b
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITAgentSessionEvent, ITAgentSessionEvent interface [TAPI 2.2], ITAgentSessionEvent interface [TAPI 2.2],described, _tapi3_itagentsessionevent, tapi3.itagentsessionevent, tapi3cc/ITAgentSessionEvent
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
 - ITAgentSessionEvent
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITAgentSessionEvent interface


## -description


The 
<b>ITAgentSessionEvent</b> interface contains methods that retrieve the description of agent session events. When the application's implementation of the 
<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a> equal to <b>TE_AGENTSESSION</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITAgentSessionEvent</b> interface. The methods of this interface can be used to retrieve information concerning the agent session change that has occurred.

See 
<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a> for additional information.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://msdn.microsoft.com/126ec551-aade-47d8-987f-1f735f10bd28">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_AGENTSESSION</b> event to enable reception of agent session events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff543067">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentSessionEvent</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITAgentSessionEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAgentSessionEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34779590-c2f6-4bd7-932b-5ac6365bcb20">get_Event</a>
</td>
<td align="left" width="63%">
Gets an 
<a href="https://msdn.microsoft.com/44eb7669-6c0b-4b9c-a209-9f15f27a1ba9">AGENT_SESSION_EVENT</a> descriptor of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2868e5db-f596-424d-bd6a-0f0c5f52e1e7">get_Session</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/6b24e8aa-fef4-44aa-8d2b-33b9be3d6ea7">About Call Center Controls</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/b0db0834-7b9b-4a72-9cc6-6cba31ed1275">ITAgentSession</a>



<a href="https://msdn.microsoft.com/8cd57c81-cd71-4fe5-a176-805c96c06c31">ITTAPIEventNotification::Event</a>



<a href="https://msdn.microsoft.com/e7662a26-d7b2-4bff-aa72-e38b58bc15df">Register Events code snippet</a>



<a href="https://msdn.microsoft.com/94faa4a1-7d86-48bc-9e94-f2b8f83f5280">TAPI_EVENT</a>
 

 

