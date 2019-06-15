---
UID: NN:tapi3if.ITCallMediaEvent
title: ITCallMediaEvent (tapi3if.h)
author: windows-sdk-content
description: The ITCallMediaEvent interface contains methods that retrieve the description of media events.
old-location: tapi3\itcallmediaevent.htm
tech.root: Tapi
ms.assetid: db55ff03-9271-4a94-9cba-a3ef0282b7b6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITCallMediaEvent, ITCallMediaEvent interface [TAPI 2.2], ITCallMediaEvent interface [TAPI 2.2],described, _tapi3_itcallmediaevent, tapi3.itcallmediaevent, tapi3if/ITCallMediaEvent
ms.topic: interface
f1_keywords: ["tapi3if/ITCallMediaEvent"]
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
 - ITCallMediaEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITCallMediaEvent interface


## -description


The 
<b>ITCallMediaEvent</b> interface contains methods that retrieve the description of media events. When the application's implementation of the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a> method indicates a 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> equal to <b>TE_CALLMEDIA</b>, the method's <i>pEvent</i> parameter is an <b>IDispatch</b> pointer for the 
<b>ITCallMediaEvent</b> interface. The methods of this interface can be used to retrieve information concerning the call media event that has occurred.
<div class="alert"><b>Note</b>  You must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method and set an event filter mask that includes the <b>TE_CALLMEDIA</b> event to enable reception of call media events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events. For more information, see the 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/events">Events</a> overview.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITCallMediaEvent</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallMediaEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITCallMediaEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_call">get_Call</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_cause">get_Cause</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event_cause">CALL_MEDIA_EVENT_CAUSE</a> for the event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_error">get_Error</a>
</td>
<td align="left" width="63%">
Gets the error associated with the media event, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_event">get_Event</a>
</td>
<td align="left" width="63%">
Gets the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a> descriptor of an event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_stream">get_Stream</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itcallmediaevent-get_terminal">get_Terminal</a>
</td>
<td align="left" width="63%">
Gets a pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-callhub_event">CALLHUB_EVENT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event">CALL_MEDIA_EVENT</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-call_media_event_cause">CALL_MEDIA_EVENT_CAUSE</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/call-object">Call Object</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ittapieventnotification-event">ITTAPIEventNotification::Event</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>
 

 

