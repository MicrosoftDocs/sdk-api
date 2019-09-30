---
UID: NN:tapi3if.ITCallStateEvent
title: ITCallStateEvent (tapi3if.h)
author: windows-sdk-content
description: The ITCallStateEvent interface contains methods that retrieve the description of call state events.
old-location: tapi3\itcallstateevent.htm
tech.root: Tapi
ms.assetid: 0885ef81-726d-41ca-be8c-b3ff2e02fc3c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallStateEvent, ITCallStateEvent interface [TAPI 2.2], ITCallStateEvent interface [TAPI 2.2],described, _tapi3_itcallstateevent, tapi3.itcallstateevent, tapi3if/ITCallStateEvent
ms.topic: interface
f1_keywords: 
 - "tapi3if/ITCallStateEvent"
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
 - ITCallStateEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallStateEvent interface


## -description


The 
<b>ITCallStateEvent</b> interface contains methods that retrieve the description of call state events. When the application's implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_CALLSTATE</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallStateEvent</b> interface. The methods of this interface can be used to retrieve information concerning the change that has occurred in the call state.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLSTATE</b> event to enable reception of call state events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallStateEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallStateEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallStateEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_callbackinstance">get_CallbackInstance</a>
</td>
<td align="left" width="63%">
Gets the callback instance associated with the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_cause">get_Cause</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_state_event_cause">CALL_STATE_EVENT_CAUSE</a> descriptor of the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallstateevent-get_state">get_State</a>
</td>
<td align="left" width="63%">
Gets a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_state">CALL_STATE</a> descriptor of the event.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_state">CALL_STATE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_state_event_cause">CALL_STATE_EVENT_CAUSE</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
 

 

