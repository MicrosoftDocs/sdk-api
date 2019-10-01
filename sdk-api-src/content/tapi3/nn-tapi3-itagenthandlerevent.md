---
UID: NN:tapi3.ITAgentHandlerEvent
title: ITAgentHandlerEvent (tapi3.h)
author: windows-sdk-content
description: The ITAgentHandlerEvent interface contains methods that retrieve the description of agent handler events.
old-location: tapi3\itagenthandlerevent.htm
tech.root: Tapi
ms.assetid: c61becce-09fd-4b12-bbc9-98df57d5f0d3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITAgentHandlerEvent, ITAgentHandlerEvent interface [TAPI 2.2], ITAgentHandlerEvent interface [TAPI 2.2],described, _tapi3_itagenthandlerevent, tapi3.itagenthandlerevent, tapi3cc/ITAgentHandlerEvent
ms.topic: interface
f1_keywords: 
 - "tapi3/ITAgentHandlerEvent"
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
 - ITAgentHandlerEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITAgentHandlerEvent interface


## -description


The 
<b>ITAgentHandlerEvent</b> interface contains methods that retrieve the description of agent handler events. When the application's implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_AGENTHANDLER</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITAgentHandlerEvent</b> interface. The methods of this interface can be used to retrieve information concerning the agent handler change that has occurred.

See 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_AGENTHANDLER</b> event to enable reception of agent handler events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentHandlerEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentHandlerEvent</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandlerevent-get_agenthandler">get_AgentHandler</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nf-tapi3-itagenthandlerevent-get_event">get_Event</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agenthandler_event">AGENTHANDLER_EVENT</a> descriptor of the event.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/ne-tapi3-agenthandler_event">AGENTHANDLER_EVENT</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
 

 

