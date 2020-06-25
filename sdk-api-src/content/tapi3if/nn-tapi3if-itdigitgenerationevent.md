---
UID: NN:tapi3if.ITDigitGenerationEvent
title: ITDigitGenerationEvent (tapi3if.h)
description: The ITDigitGenerationEvent interface contains methods that describe digit generation events.
helpviewer_keywords: ["ITDigitGenerationEvent","ITDigitGenerationEvent interface [TAPI 2.2]","ITDigitGenerationEvent interface [TAPI 2.2]","described","_tapi3_itdigitgenerationevent","tapi3.itdigitgenerationevent","tapi3if/ITDigitGenerationEvent"]
old-location: tapi3\itdigitgenerationevent.htm
tech.root: Tapi
ms.assetid: 788eee9c-b885-4b94-b259-694353c0f63a
ms.date: 12/05/2018
ms.keywords: ITDigitGenerationEvent, ITDigitGenerationEvent interface [TAPI 2.2], ITDigitGenerationEvent interface [TAPI 2.2],described, _tapi3_itdigitgenerationevent, tapi3.itdigitgenerationevent, tapi3if/ITDigitGenerationEvent
f1_keywords:
- tapi3if/ITDigitGenerationEvent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Tapi3.dll
api_name:
- ITDigitGenerationEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDigitGenerationEvent interface


## -description


The 
<b>ITDigitGenerationEvent</b> interface contains methods that describe digit generation events. When the application's implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_GENERATEEVENT</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITDigitGenerationEvent</b> interface. The methods of this interface can be used to report on calls that require the generation of DTMF digits. This interface is implemented by the application and called by the TAPI 3 DLL.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_GENERATEEVENT</b> event to enable reception of digit generation events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDigitGenerationEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDigitGenerationEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDigitGenerationEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitgenerationevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitgenerationevent-get_callbackinstance">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitgenerationevent-get_generationtermination">get_GenerationTermination</a>
</td>
<td align="left" width="63%">
Gets the digit or digits that indicate the end of the generated digit series.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itdigitgenerationevent-get_tickcount">get_TickCount</a>
</td>
<td align="left" width="63%">
Gets the "tick count" (number of milliseconds since Windows started) at which the digit-gathering completed.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/register-events">Register Events code snippet</a>
 

 

