---
UID: NF:tapi3if.ITTAPIEventNotification.Event
title: ITTAPIEventNotification::Event (tapi3if.h)
description: The Event method is called by TAPI to determine the response to an asynchronous event notification.
helpviewer_keywords: ["Event","Event method [TAPI 2.2]","Event method [TAPI 2.2]","ITTAPIEventNotification interface","ITTAPIEventNotification interface [TAPI 2.2]","Event method","ITTAPIEventNotification.Event","ITTAPIEventNotification::Event","_tapi3_ittapieventnotification_event","tapi3.ittapieventnotification_event","tapi3if/ITTAPIEventNotification::Event"]
old-location: tapi3\ittapieventnotification_event.htm
tech.root: tapi3
ms.assetid: 8cd57c81-cd71-4fe5-a176-805c96c06c31
ms.date: 12/05/2018
ms.keywords: Event, Event method [TAPI 2.2], Event method [TAPI 2.2],ITTAPIEventNotification interface, ITTAPIEventNotification interface [TAPI 2.2],Event method, ITTAPIEventNotification.Event, ITTAPIEventNotification::Event, _tapi3_ittapieventnotification_event, tapi3.ittapieventnotification_event, tapi3if/ITTAPIEventNotification::Event
req.header: tapi3if.h
req.include-header: 
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
 - ITTAPIEventNotification::Event
 - tapi3if/ITTAPIEventNotification::Event
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
 - ITTAPIEventNotification.Event
---

# ITTAPIEventNotification::Event


## -description

The 
<b>Event</b> method is called by TAPI to determine the response to an asynchronous event notification. The application implements a set of case statements that use <i>TapiEvent</i> to determine the type of event being signaled, then calls <b>IUnknown::QueryInterface</b> on <i>pEvent</i> to obtain the appropriate event interface pointer. Each event defined by TAPI 3 has an interface associated with it. The specific events handled depend on the needs of the application.

## -parameters

### -param TapiEvent [in]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a> indicator of the event.

### -param pEvent [in]

Pointer to an <b>IDispatch</b> interface of the object associated with this event.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>

## -remarks

You must call the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter">ITTAPI::put_EventFilter</a> method to set the event filter mask and enable reception of events. If you do not call <b>ITTAPI::put_EventFilter</b>, your application will not receive any events.

## -see-also

<a href="/windows/desktop/Tapi/events">Events overview</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapieventnotification">ITTAPIEventNotification</a>



<a href="/windows/desktop/Tapi/register-events">Register Events code snippet</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapi_event">TAPI_EVENT</a>