---
UID: NN:tapi3cc.ITQueueEvent
title: ITQueueEvent (tapi3cc.h)
description: The ITQueueEvent interface (tapi3cc.h) contains methods that retrieve the description of Automatic Call Distribution (ACD) queue events.
helpviewer_keywords: ["ITQueueEvent","ITQueueEvent interface [TAPI 2.2]","ITQueueEvent interface [TAPI 2.2]","described","_tapi3_itqueueevent","tapi3.itqueueevent","tapi3cc/ITQueueEvent"]
old-location: tapi3\itqueueevent.htm
tech.root: tapi3
ms.assetid: 7e4655ff-6ed4-4166-91f7-49d2e0556662
ms.date: 08/10/2022
ms.keywords: ITQueueEvent, ITQueueEvent interface [TAPI 2.2], ITQueueEvent interface [TAPI 2.2],described, _tapi3_itqueueevent, tapi3.itqueueevent, tapi3cc/ITQueueEvent
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
 - ITQueueEvent
 - tapi3cc/ITQueueEvent
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
 - ITQueueEvent
---

# ITQueueEvent interface


## -description

The 
<b>ITQueueEvent</b> interface contains methods that retrieve the description of Automatic Call Distribution (ACD) queue events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_QUEUE</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITQueueEvent</b> interface. The methods of this interface can be used to retrieve information concerning a queue event that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_QUEUE</b> event to enable reception of ACD queue events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITQueueEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITQueueEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3/ne-tapi3-acdqueue_event">ACDQUEUE_EVENT</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3cc/nn-tapi3cc-itqueue">ITQueue</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
