---
UID: NF:tapi3if.ITCallNotificationEvent.get_Event
title: ITCallNotificationEvent::get_Event (tapi3if.h)
description: The get_Event method returns a CALL_NOTIFICATION_EVENT description of whether the application owns or is monitoring the call on which the event has occurred.
helpviewer_keywords: ["ITCallNotificationEvent interface [TAPI 2.2]","get_Event method","ITCallNotificationEvent.get_Event","ITCallNotificationEvent::get_Event","_tapi3_itcallnotificationevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITCallNotificationEvent interface","tapi3.itcallnotificationevent_get_event","tapi3if/ITCallNotificationEvent::get_Event"]
old-location: tapi3\itcallnotificationevent_get_event.htm
tech.root: tapi3
ms.assetid: 08a3925c-e14e-442e-952e-483fc41d049c
ms.date: 12/05/2018
ms.keywords: ITCallNotificationEvent interface [TAPI 2.2],get_Event method, ITCallNotificationEvent.get_Event, ITCallNotificationEvent::get_Event, _tapi3_itcallnotificationevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITCallNotificationEvent interface, tapi3.itcallnotificationevent_get_event, tapi3if/ITCallNotificationEvent::get_Event
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
 - ITCallNotificationEvent::get_Event
 - tapi3if/ITCallNotificationEvent::get_Event
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
 - ITCallNotificationEvent.get_Event
---

# ITCallNotificationEvent::get_Event


## -description

The 
<b>get_Event</b> method returns a 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_notification_event">CALL_NOTIFICATION_EVENT</a> description of whether the application owns or is monitoring the call on which the event has occurred.

## -parameters

### -param pCallNotificationEvent [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_notification_event">CALL_NOTIFICATION_EVENT</a> description of the application's privilege on the call returned by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallnotificationevent-get_call">ITCallNotificationEvent::get_Call</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pCallNotificationEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-call_notification_event">CALL_NOTIFICATION_EVENT</a>



<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>