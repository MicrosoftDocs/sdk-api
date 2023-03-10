---
UID: NN:tapi3if.ITCallStateEvent
title: ITCallStateEvent (tapi3if.h)
description: The ITCallStateEvent interface contains methods that retrieve the description of call state events.
helpviewer_keywords: ["ITCallStateEvent","ITCallStateEvent interface [TAPI 2.2]","ITCallStateEvent interface [TAPI 2.2]","described","_tapi3_itcallstateevent","tapi3.itcallstateevent","tapi3if/ITCallStateEvent"]
old-location: tapi3\itcallstateevent.htm
tech.root: tapi3
ms.assetid: 0885ef81-726d-41ca-be8c-b3ff2e02fc3c
ms.date: 12/05/2018
ms.keywords: ITCallStateEvent, ITCallStateEvent interface [TAPI 2.2], ITCallStateEvent interface [TAPI 2.2],described, _tapi3_itcallstateevent, tapi3.itcallstateevent, tapi3if/ITCallStateEvent
req.header: tapi3if.h
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
 - ITCallStateEvent
 - tapi3if/ITCallStateEvent
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
 - ITCallStateEvent
---

# ITCallStateEvent interface


## -description

The 
<b>ITCallStateEvent</b> interface contains methods that retrieve the description of call state events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_CALLSTATE</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallStateEvent</b> interface. The methods of this interface can be used to retrieve information concerning the change that has occurred in the call state.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLSTATE</b> event to enable reception of call state events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITCallStateEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallStateEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state">CALL_STATE</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_state_event_cause">CALL_STATE_EVENT_CAUSE</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
