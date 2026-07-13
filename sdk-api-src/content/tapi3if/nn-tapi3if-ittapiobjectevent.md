---
UID: NN:tapi3if.ITTAPIObjectEvent
title: ITTAPIObjectEvent (tapi3if.h)
description: The ITTAPIObjectEvent interface contains methods that retrieve the description of TAPI object events.
helpviewer_keywords: ["ITTAPIObjectEvent","ITTAPIObjectEvent interface [TAPI 2.2]","ITTAPIObjectEvent interface [TAPI 2.2]","described","_tapi3_ittapiobjectevent","tapi3.ittapiobjectevent","tapi3if/ITTAPIObjectEvent"]
old-location: tapi3\ittapiobjectevent.htm
tech.root: tapi3
ms.assetid: 73be7109-0d3a-4ac5-adb7-e1577d8640b5
ms.date: 12/05/2018
ms.keywords: ITTAPIObjectEvent, ITTAPIObjectEvent interface [TAPI 2.2], ITTAPIObjectEvent interface [TAPI 2.2],described, _tapi3_ittapiobjectevent, tapi3.ittapiobjectevent, tapi3if/ITTAPIObjectEvent
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
 - ITTAPIObjectEvent
 - tapi3if/ITTAPIObjectEvent
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
 - ITTAPIObjectEvent
---

# ITTAPIObjectEvent interface


## -description

The 
<b>ITTAPIObjectEvent</b> interface contains methods that retrieve the description of TAPI object events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_TAPIOBJECT</b>, the method's <i>pEvent</i> parameter is an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointer for the 
<b>ITTAPIObjectEvent</b> interface. The methods of this interface can be used to retrieve information concerning the TAPI object change that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_TAPIOBJECT</b> event to enable reception of TAPI object events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2">ITTAPIObjectEvent2</a> interface is an extension of the 
<b>ITTAPIObjectEvent</b> interface. 
<b>ITTAPIObjectEvent2</b> exposes an additional method that returns a pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface on the phone object that caused the TAPI object event.

## -inheritance

The <b>ITTAPIObjectEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPIObjectEvent</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent2">ITTAPIObjectEvent2</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
