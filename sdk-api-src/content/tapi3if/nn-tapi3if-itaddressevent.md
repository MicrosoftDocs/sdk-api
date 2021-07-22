---
UID: NN:tapi3if.ITAddressEvent
title: ITAddressEvent (tapi3if.h)
description: The ITAddressEvent interface contains methods that retrieve the description of address events.
helpviewer_keywords: ["ITAddressEvent","ITAddressEvent interface [TAPI 2.2]","ITAddressEvent interface [TAPI 2.2]","described","_tapi3_itaddressevent","tapi3.itaddressevent","tapi3if/ITAddressEvent"]
old-location: tapi3\itaddressevent.htm
tech.root: tapi3
ms.assetid: 340d938a-a107-4317-af65-3dca98102767
ms.date: 12/05/2018
ms.keywords: ITAddressEvent, ITAddressEvent interface [TAPI 2.2], ITAddressEvent interface [TAPI 2.2],described, _tapi3_itaddressevent, tapi3.itaddressevent, tapi3if/ITAddressEvent
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
 - ITAddressEvent
 - tapi3if/ITAddressEvent
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
 - ITAddressEvent
---

# ITAddressEvent interface


## -description

The 
<b>ITAddressEvent</b> interface contains methods that retrieve the description of address events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_ADDRESS</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITAddressEvent</b> interface. The methods of this interface can be used to retrieve information concerning the type of event, which address the event has occurred on, and for which terminal.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_ADDRESS</b> event to enable reception of address events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITAddressEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAddressEvent</b> also has these types of members:

## -remarks

Certain events on PnP devices will not be received until after the first time static terminals are enumerated using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">ITTerminalSupport::EnumerateStaticTerminals</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals">ITTerminalSupport::get_StaticTerminals</a>.

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_event">ADDRESS_EVENT</a>



<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/Tapi/device-events-ovr">Device Events overview</a>



<a href="/windows/desktop/Tapi/event-notification">Event Notification overview</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
