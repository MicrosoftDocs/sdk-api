---
UID: NF:tapi3if.ITCallNotificationEvent.get_CallbackInstance
title: ITCallNotificationEvent::get_CallbackInstance (tapi3if.h)
description: The get_CallbackInstance method gets a pointer to the callback instance associated with this event. (ITCallNotificationEvent.get_CallbackInstance)
helpviewer_keywords: ["ITCallNotificationEvent interface [TAPI 2.2]","get_CallbackInstance method","ITCallNotificationEvent.get_CallbackInstance","ITCallNotificationEvent::get_CallbackInstance","_tapi3_itcallnotificationevent_get_callbackinstance","get_CallbackInstance","get_CallbackInstance method [TAPI 2.2]","get_CallbackInstance method [TAPI 2.2]","ITCallNotificationEvent interface","tapi3.itcallnotificationevent_get_callbackinstance","tapi3if/ITCallNotificationEvent::get_CallbackInstance"]
old-location: tapi3\itcallnotificationevent_get_callbackinstance.htm
tech.root: tapi3
ms.assetid: daa6d980-49aa-4e5a-9871-77e39dcdb6f0
ms.date: 12/05/2018
ms.keywords: ITCallNotificationEvent interface [TAPI 2.2],get_CallbackInstance method, ITCallNotificationEvent.get_CallbackInstance, ITCallNotificationEvent::get_CallbackInstance, _tapi3_itcallnotificationevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITCallNotificationEvent interface, tapi3.itcallnotificationevent_get_callbackinstance, tapi3if/ITCallNotificationEvent::get_CallbackInstance
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
 - ITCallNotificationEvent::get_CallbackInstance
 - tapi3if/ITCallNotificationEvent::get_CallbackInstance
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
 - ITCallNotificationEvent.get_CallbackInstance
---

# ITCallNotificationEvent::get_CallbackInstance


## -description

The 
<b>get_CallbackInstance</b> method gets a pointer to the callback instance associated with this event.

## -parameters

### -param plCallbackInstance [out]

Pointer to callback instance returned by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>.

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
The <i>plCallbackInstance</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallnotificationevent">ITCallNotificationEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>
