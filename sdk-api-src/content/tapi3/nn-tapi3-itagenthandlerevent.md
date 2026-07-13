---
UID: NN:tapi3.ITAgentHandlerEvent
title: ITAgentHandlerEvent (tapi3.h)
description: The ITAgentHandlerEvent (tapi3.h) interface contains methods that retrieve the description of agent handler events.
helpviewer_keywords: ["ITAgentHandlerEvent","ITAgentHandlerEvent interface [TAPI 2.2]","ITAgentHandlerEvent interface [TAPI 2.2]","described","_tapi3_itagenthandlerevent","tapi3.itagenthandlerevent","tapi3cc/ITAgentHandlerEvent"]
old-location: tapi3\itagenthandlerevent.htm
tech.root: tapi3
ms.assetid: c61becce-09fd-4b12-bbc9-98df57d5f0d3
ms.date: 08/10/2022
ms.keywords: ITAgentHandlerEvent, ITAgentHandlerEvent interface [TAPI 2.2], ITAgentHandlerEvent interface [TAPI 2.2],described, _tapi3_itagenthandlerevent, tapi3.itagenthandlerevent, tapi3cc/ITAgentHandlerEvent
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
 - ITAgentHandlerEvent
 - tapi3/ITAgentHandlerEvent
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
 - ITAgentHandlerEvent
---

# ITAgentHandlerEvent interface


## -description

The 
<b>ITAgentHandlerEvent</b> interface contains methods that retrieve the description of agent handler events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_AGENTHANDLER</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITAgentHandlerEvent</b> interface. The methods of this interface can be used to retrieve information concerning the agent handler change that has occurred.

See 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_AGENTHANDLER</b> event to enable reception of agent handler events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITAgentHandlerEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentHandlerEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-agenthandler_event">AGENTHANDLER_EVENT</a>



<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagent">ITAgent</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagenthandler">ITAgentHandler</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
