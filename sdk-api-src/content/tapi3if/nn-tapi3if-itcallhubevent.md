---
UID: NN:tapi3if.ITCallHubEvent
title: ITCallHubEvent (tapi3if.h)
description: The ITCallHubEvent interface contains methods that retrieve the description of CallHub events.
helpviewer_keywords: ["ITCallHubEvent","ITCallHubEvent interface [TAPI 2.2]","ITCallHubEvent interface [TAPI 2.2]","described","_tapi3_itcallhubevent","tapi3.itcallhubevent","tapi3if/ITCallHubEvent"]
old-location: tapi3\itcallhubevent.htm
tech.root: tapi3
ms.assetid: 4008fc7e-f095-442d-9214-61bfead8cf04
ms.date: 12/05/2018
ms.keywords: ITCallHubEvent, ITCallHubEvent interface [TAPI 2.2], ITCallHubEvent interface [TAPI 2.2],described, _tapi3_itcallhubevent, tapi3.itcallhubevent, tapi3if/ITCallHubEvent
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
 - ITCallHubEvent
 - tapi3if/ITCallHubEvent
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
 - ITCallHubEvent
---

# ITCallHubEvent interface


## -description

The 
<b>ITCallHubEvent</b> interface contains methods that retrieve the description of CallHub events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_CALLHUB</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallHubEvent</b> interface. The methods of this interface can be used to retrieve information concerning the CallHub change that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLHUB</b> event to enable reception of CallHub events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITCallHubEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallHubEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-callhub_event">CALLHUB_EVENT</a>



<a href="/windows/desktop/Tapi/callhub-object">CallHub Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallhub">ITCallHub</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
