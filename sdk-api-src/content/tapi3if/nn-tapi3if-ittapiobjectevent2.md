---
UID: NN:tapi3if.ITTAPIObjectEvent2
title: ITTAPIObjectEvent2 (tapi3if.h)
description: The ITTAPIObjectEvent2 interface is an extension of the ITTAPIObjectEvent interface. ITTAPIObjectEvent2 exposes an additional method that returns a pointer to an ITPhone interface on the phone object that caused the TAPI object event.
helpviewer_keywords: ["ITTAPIObjectEvent2","ITTAPIObjectEvent2 interface [TAPI 2.2]","ITTAPIObjectEvent2 interface [TAPI 2.2]","described","_tapi3_ittapiobjectevent2","tapi3.ittapiobjectevent2","tapi3if/ITTAPIObjectEvent2"]
old-location: tapi3\ittapiobjectevent2.htm
tech.root: tapi3
ms.assetid: ad4fc838-5a6c-4942-b5a0-ed00cea11ba8
ms.date: 12/05/2018
ms.keywords: ITTAPIObjectEvent2, ITTAPIObjectEvent2 interface [TAPI 2.2], ITTAPIObjectEvent2 interface [TAPI 2.2],described, _tapi3_ittapiobjectevent2, tapi3.ittapiobjectevent2, tapi3if/ITTAPIObjectEvent2
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
 - ITTAPIObjectEvent2
 - tapi3if/ITTAPIObjectEvent2
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
 - ITTAPIObjectEvent2
---

# ITTAPIObjectEvent2 interface


## -description

The 
<b>ITTAPIObjectEvent2</b> interface is an extension of the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a> interface. 
<b>ITTAPIObjectEvent2</b> exposes an additional method that returns a pointer to an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface on the phone object that caused the TAPI object event.

When the application's implementation of the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_TAPIOBJECT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITTAPIObjectEvent2</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_TAPIOBJECT</b> event to enable reception of TAPI object events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b>ITTAPIObjectEvent2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTAPIObjectEvent2</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a>
