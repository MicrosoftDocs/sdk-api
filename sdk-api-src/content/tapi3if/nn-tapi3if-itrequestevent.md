---
UID: NN:tapi3if.ITRequestEvent
title: ITRequestEvent (tapi3if.h)
description: The ITRequestEvent interface contains methods that allow an application to receive and process Assisted Telephony request events.
helpviewer_keywords: ["ITRequestEvent","ITRequestEvent interface [TAPI 2.2]","ITRequestEvent interface [TAPI 2.2]","described","_tapi3_itrequestevent","tapi3.itrequestevent","tapi3if/ITRequestEvent"]
old-location: tapi3\itrequestevent.htm
tech.root: tapi3
ms.assetid: 69f9b504-be01-4167-8002-32a8e86bab0f
ms.date: 12/05/2018
ms.keywords: ITRequestEvent, ITRequestEvent interface [TAPI 2.2], ITRequestEvent interface [TAPI 2.2],described, _tapi3_itrequestevent, tapi3.itrequestevent, tapi3if/ITRequestEvent
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
 - ITRequestEvent
 - tapi3if/ITRequestEvent
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
 - ITRequestEvent
---

# ITRequestEvent interface


## -description

The 
<b>ITRequestEvent</b> interface contains methods that allow an application to receive and process 
<a href="/windows/desktop/Tapi/assisted-telephony-overview">Assisted Telephony</a> request events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_REQUEST</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITRequestEvent</b> interface. The methods of this interface can be used to retrieve information concerning a request event that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_REQUEST</b> event to enable reception of request events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITRequestEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITRequestEvent</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itrequest">ITRequest</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
