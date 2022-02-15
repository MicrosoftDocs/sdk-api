---
UID: NN:tapi3if.ITCallMediaEvent
title: ITCallMediaEvent (tapi3if.h)
description: The ITCallMediaEvent interface contains methods that retrieve the description of media events.
helpviewer_keywords: ["ITCallMediaEvent","ITCallMediaEvent interface [TAPI 2.2]","ITCallMediaEvent interface [TAPI 2.2]","described","_tapi3_itcallmediaevent","tapi3.itcallmediaevent","tapi3if/ITCallMediaEvent"]
old-location: tapi3\itcallmediaevent.htm
tech.root: tapi3
ms.assetid: db55ff03-9271-4a94-9cba-a3ef0282b7b6
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent, ITCallMediaEvent interface [TAPI 2.2], ITCallMediaEvent interface [TAPI 2.2],described, _tapi3_itcallmediaevent, tapi3.itcallmediaevent, tapi3if/ITCallMediaEvent
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
 - ITCallMediaEvent
 - tapi3if/ITCallMediaEvent
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
 - ITCallMediaEvent
---

# ITCallMediaEvent interface


## -description

The 
<b>ITCallMediaEvent</b> interface contains methods that retrieve the description of media events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_CALLMEDIA</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallMediaEvent</b> interface. The methods of this interface can be used to retrieve information concerning the call media event that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLMEDIA</b> event to enable reception of call media events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITCallMediaEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallMediaEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callhub_event">CALLHUB_EVENT</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event_cause">CALL_MEDIA_EVENT_CAUSE</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
