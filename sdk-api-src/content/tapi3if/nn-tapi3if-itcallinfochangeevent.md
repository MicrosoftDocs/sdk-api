---
UID: NN:tapi3if.ITCallInfoChangeEvent
title: ITCallInfoChangeEvent (tapi3if.h)
description: The ITCallInfoChangeEvent interface contains methods that retrieve the description of call information change events.
helpviewer_keywords: ["ITCallInfoChangeEvent","ITCallInfoChangeEvent interface [TAPI 2.2]","ITCallInfoChangeEvent interface [TAPI 2.2]","described","_tapi3_itcallinfochangeevent","tapi3.itcallinfochangeevent","tapi3if/ITCallInfoChangeEvent"]
old-location: tapi3\itcallinfochangeevent.htm
tech.root: tapi3
ms.assetid: f543da95-c0cc-4631-b91e-ba02dde2c081
ms.date: 12/05/2018
ms.keywords: ITCallInfoChangeEvent, ITCallInfoChangeEvent interface [TAPI 2.2], ITCallInfoChangeEvent interface [TAPI 2.2],described, _tapi3_itcallinfochangeevent, tapi3.itcallinfochangeevent, tapi3if/ITCallInfoChangeEvent
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
 - ITCallInfoChangeEvent
 - tapi3if/ITCallInfoChangeEvent
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
 - ITCallInfoChangeEvent
---

# ITCallInfoChangeEvent interface


## -description

The 
<b>ITCallInfoChangeEvent</b> interface contains methods that retrieve the description of call information change events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_CALLINFOCHANGE</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallInfoChangeEvent</b> interface. The methods of this interface can be used to retrieve information concerning the call information that has changed.

The 
<b>ITCallInfoChangeEvent</b> is an outgoing interface. This interface is registered with the TAPI object to get all information about calls. An application must have called the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a> method on the TAPI object before registering this interface. If not, the call to <b>Advise</b> will fail. This interface cannot be unregistered—<b>Unadvise</b> will always fail.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLINFOCHANGE</b> event to enable reception of call information change events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITCallInfoChangeEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallInfoChangeEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
