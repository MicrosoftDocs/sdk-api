---
UID: NN:tapi3.ITAgentEvent
title: ITAgentEvent (tapi3.h)
description: The ITAgentEvent interface contains methods that retrieve the description of agent events.
helpviewer_keywords: ["ITAgentEvent","ITAgentEvent interface [TAPI 2.2]","ITAgentEvent interface [TAPI 2.2]","described","_tapi3_itagentevent","tapi3.itagentevent","tapi3cc/ITAgentEvent"]
old-location: tapi3\itagentevent.htm
tech.root: tapi3
ms.assetid: adfb58f7-b02c-4a64-92c1-a1b29c9f7143
ms.date: 12/05/2018
ms.keywords: ITAgentEvent, ITAgentEvent interface [TAPI 2.2], ITAgentEvent interface [TAPI 2.2],described, _tapi3_itagentevent, tapi3.itagentevent, tapi3cc/ITAgentEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAgentEvent
 - tapi3/ITAgentEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentEvent
---

# ITAgentEvent interface


## -description

The 
<b>ITAgentEvent</b> interface contains methods that retrieve the description of agent events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_AGENT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITAgentEvent</b> interface. The methods of this interface can be used to retrieve information concerning the agent event that has occurred.

See 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information on agents.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_AGENT</b> event to enable reception of agent events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITAgentEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITAgentEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagentevent-get_agent">get_Agent</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagentevent-get_event">get_Event</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_event">AGENT_EVENT</a> descriptor of an event.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-agent_event">AGENT_EVENT</a>



<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>