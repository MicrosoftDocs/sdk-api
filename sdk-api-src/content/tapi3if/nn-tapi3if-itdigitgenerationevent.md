---
UID: NN:tapi3if.ITDigitGenerationEvent
title: ITDigitGenerationEvent (tapi3if.h)
description: The ITDigitGenerationEvent interface contains methods that describe digit generation events.
helpviewer_keywords: ["ITDigitGenerationEvent","ITDigitGenerationEvent interface [TAPI 2.2]","ITDigitGenerationEvent interface [TAPI 2.2]","described","_tapi3_itdigitgenerationevent","tapi3.itdigitgenerationevent","tapi3if/ITDigitGenerationEvent"]
old-location: tapi3\itdigitgenerationevent.htm
tech.root: tapi3
ms.assetid: 788eee9c-b885-4b94-b259-694353c0f63a
ms.date: 12/05/2018
ms.keywords: ITDigitGenerationEvent, ITDigitGenerationEvent interface [TAPI 2.2], ITDigitGenerationEvent interface [TAPI 2.2],described, _tapi3_itdigitgenerationevent, tapi3.itdigitgenerationevent, tapi3if/ITDigitGenerationEvent
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
 - ITDigitGenerationEvent
 - tapi3if/ITDigitGenerationEvent
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
 - ITDigitGenerationEvent
---

# ITDigitGenerationEvent interface


## -description

The 
<b>ITDigitGenerationEvent</b> interface contains methods that describe digit generation events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_GENERATEEVENT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITDigitGenerationEvent</b> interface. The methods of this interface can be used to report on calls that require the generation of DTMF digits. This interface is implemented by the application and called by the TAPI 3 DLL.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_GENERATEEVENT</b> event to enable reception of digit generation events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITDigitGenerationEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDigitGenerationEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/events">Events</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>
