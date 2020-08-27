---
UID: NN:tapi3if.ITPhoneEvent
title: ITPhoneEvent (tapi3if.h)
description: The ITPhoneEvent interface contains methods that retrieve the description of phone events that have occurred.
helpviewer_keywords: ["ITPhoneEvent","ITPhoneEvent interface [TAPI 2.2]","ITPhoneEvent interface [TAPI 2.2]","described","_tapi3_itphoneevent","tapi3.itphoneevent","tapi3if/ITPhoneEvent"]
old-location: tapi3\itphoneevent.htm
tech.root: tapi3
ms.assetid: cc3ca533-d523-4889-b3c7-bb306e49b85b
ms.date: 12/05/2018
ms.keywords: ITPhoneEvent, ITPhoneEvent interface [TAPI 2.2], ITPhoneEvent interface [TAPI 2.2],described, _tapi3_itphoneevent, tapi3.itphoneevent, tapi3if/ITPhoneEvent
f1_keywords:
- tapi3if/ITPhoneEvent
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
- ITPhoneEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITPhoneEvent interface


## -description


The 
<b>ITPhoneEvent</b> interface contains methods that retrieve the description of phone events that have occurred. When the application's implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_PHONEEVENT</b>, the method's <i>pEvent</i> parameter is an 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> pointer for the 
<b>ITPhoneEvent</b> interface.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes <b>TE_PHONEEVENT</b> to enable reception of phone events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITPhoneEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITPhoneEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITPhoneEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_buttonlampid">get_ButtonLampId</a>
</td>
<td align="left" width="63%">
Gets a long value indicating which button or lamp triggered the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_buttonstate">get_ButtonState</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_button_state">PHONE_BUTTON_STATE</a> value specifying the state to which the button has transitioned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface for the call object involved in the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_event">get_Event</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_event">PHONE_EVENT</a> value specifying the type of phone event that occurred.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_hookswitchdevice">get_HookSwitchDevice</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_device">PHONE_HOOK_SWITCH_DEVICE</a> value specifying the hookswitch device that changed state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_hookswitchstate">get_HookSwitchState</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-phone_hook_switch_state">PHONE_HOOK_SWITCH_STATE</a> value specifying the state to which the hookswitch has transitioned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_numbergathered">get_NumberGathered</a>
</td>
<td align="left" width="63%">
Returns a <b>BSTR</b> value specifying the phone number that was gathered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_phone">get_Phone</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface on the phone object that fired this event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itphoneevent-get_ringmode">get_RingMode</a>
</td>
<td align="left" width="63%">
Gets a long value specifying the ring mode to which the phone has transitioned.

</td>
</tr>
</table> 

