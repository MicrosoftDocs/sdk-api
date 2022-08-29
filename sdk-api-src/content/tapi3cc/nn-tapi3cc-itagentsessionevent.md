---
UID: NN:tapi3cc.ITAgentSessionEvent
title: ITAgentSessionEvent (tapi3cc.h)
description: The ITAgentSessionEvent interface (tapi3cc.h) contains methods that retrieve the description of agent session events.
helpviewer_keywords: ["ITAgentSessionEvent","ITAgentSessionEvent interface [TAPI 2.2]","ITAgentSessionEvent interface [TAPI 2.2]","described","_tapi3_itagentsessionevent","tapi3.itagentsessionevent","tapi3cc/ITAgentSessionEvent"]
old-location: tapi3\itagentsessionevent.htm
tech.root: tapi3
ms.assetid: 70d37d06-b1a6-4f7e-bfe5-731d1b4cd66b
ms.date: 08/10/2022
ms.keywords: ITAgentSessionEvent, ITAgentSessionEvent interface [TAPI 2.2], ITAgentSessionEvent interface [TAPI 2.2],described, _tapi3_itagentsessionevent, tapi3.itagentsessionevent, tapi3cc/ITAgentSessionEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAgentSessionEvent
 - tapi3cc/ITAgentSessionEvent
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
 - ITAgentSessionEvent
---

# ITAgentSessionEvent interface


## -description

The 
<b>ITAgentSessionEvent</b> interface contains methods that retrieve the description of agent session events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_AGENTSESSION</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITAgentSessionEvent</b> interface. The methods of this interface can be used to retrieve information concerning the agent session change that has occurred.

See 
<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a> for additional information.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_AGENTSESSION</b> event to enable reception of agent session events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITAgentSessionEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAgentSessionEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/about-call-center-controls">About Call Center Controls</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3/nn-tapi3-itagentsession">ITAgentSession</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
