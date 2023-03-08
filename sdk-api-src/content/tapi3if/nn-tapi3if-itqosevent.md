---
UID: NN:tapi3if.ITQOSEvent
title: ITQOSEvent (tapi3if.h)
description: The ITQOSEvent interface contains methods that retrieve the description of quality of service (QOS) events.
helpviewer_keywords: ["ITQOSEvent","ITQOSEvent interface [TAPI 2.2]","ITQOSEvent interface [TAPI 2.2]","described","_tapi3_itqosevent","tapi3.itqosevent","tapi3if/ITQOSEvent"]
old-location: tapi3\itqosevent.htm
tech.root: tapi3
ms.assetid: 6e3a8aef-bd76-4047-9018-801a3cab2c62
ms.date: 12/05/2018
ms.keywords: ITQOSEvent, ITQOSEvent interface [TAPI 2.2], ITQOSEvent interface [TAPI 2.2],described, _tapi3_itqosevent, tapi3.itqosevent, tapi3if/ITQOSEvent
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
 - ITQOSEvent
 - tapi3if/ITQOSEvent
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
 - ITQOSEvent
---

# ITQOSEvent interface


## -description

The 
<b>ITQOSEvent</b> interface contains methods that retrieve the description of quality of service (QOS) events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_QOSEVENT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITQOSEvent</b> interface. The methods of this interface can be used to retrieve information concerning a QOS event that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_QOSEVENT</b> to enable reception of QOS events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITQOSEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITQOSEvent</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-qos_event">QOS_EVENT</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>



<a href="/windows/desktop/Tapi/tapimediatype--constants">media type</a>
