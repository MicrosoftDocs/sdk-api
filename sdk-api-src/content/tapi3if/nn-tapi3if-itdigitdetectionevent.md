---
UID: NN:tapi3if.ITDigitDetectionEvent
title: ITDigitDetectionEvent (tapi3if.h)
description: The ITDigitDetectionEvent interface contains methods that retrieve the description of DTMF digit events.
helpviewer_keywords: ["ITDigitDetectionEvent","ITDigitDetectionEvent interface [TAPI 2.2]","ITDigitDetectionEvent interface [TAPI 2.2]","described","_tapi3_itdigitdetectionevent","tapi3.itdigitdetectionevent","tapi3if/ITDigitDetectionEvent"]
old-location: tapi3\itdigitdetectionevent.htm
tech.root: tapi3
ms.assetid: f387f5f5-06e4-45f2-8d93-31ff0da6151a
ms.date: 12/05/2018
ms.keywords: ITDigitDetectionEvent, ITDigitDetectionEvent interface [TAPI 2.2], ITDigitDetectionEvent interface [TAPI 2.2],described, _tapi3_itdigitdetectionevent, tapi3.itdigitdetectionevent, tapi3if/ITDigitDetectionEvent
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
 - ITDigitDetectionEvent
 - tapi3if/ITDigitDetectionEvent
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
 - ITDigitDetectionEvent
---

# ITDigitDetectionEvent interface


## -description

The 
<b>ITDigitDetectionEvent</b> interface contains methods that retrieve the description of DTMF digit events. When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_DIGITEVENT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITDigitDetectionEvent</b> interface. The methods of this interface can be used to detect DTMF digits during a call. This interface is implemented by the application and called by the TAPI 3 DLL.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_DIGITEVENT</b> event to enable reception of DTMF digit events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. You must also call <a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol-detectdigits">ITLegacyCallMediaControl::DetectDigits</a> to indicate which type of digit detection is needed. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITDigitDetectionEvent</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDigitDetectionEvent</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/events">Events</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code
		  snippet</a>
