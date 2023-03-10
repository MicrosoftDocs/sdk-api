---
UID: NN:tapi3if.ITCallNotificationEvent
title: ITCallNotificationEvent (tapi3if.h)
description: The ITCallNotificationEvent interface contains methods that retrieve the description of call notification events.
helpviewer_keywords: ["ITCallNotificationEvent","ITCallNotificationEvent interface [TAPI 2.2]","ITCallNotificationEvent interface [TAPI 2.2]","described","_tapi3_itcallnotificationevent","tapi3.itcallnotificationevent","tapi3if/ITCallNotificationEvent"]
old-location: tapi3\itcallnotificationevent.htm
tech.root: tapi3
ms.assetid: d0ea4f7a-7b50-4610-ae17-957c0c1891e1
ms.date: 12/05/2018
ms.keywords: ITCallNotificationEvent, ITCallNotificationEvent interface [TAPI 2.2], ITCallNotificationEvent interface [TAPI 2.2],described, _tapi3_itcallnotificationevent, tapi3.itcallnotificationevent, tapi3if/ITCallNotificationEvent
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
 - ITCallNotificationEvent
 - tapi3if/ITCallNotificationEvent
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
 - ITCallNotificationEvent
---

# ITCallNotificationEvent interface


## -description

The 
<b>ITCallNotificationEvent</b> interface contains methods that retrieve the description of call notification events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_CALLNOTIFICATION</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallNotificationEvent</b> interface. The methods of this interface can be used to retrieve information concerning the call notification event that has occurred.

This outgoing interface is registered with the TAPI object to get all information about calls. An application must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a> method on the TAPI object before registering this interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLNOTIFICATION</b> event to enable reception of call notification events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITCallNotificationEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallNotificationEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
