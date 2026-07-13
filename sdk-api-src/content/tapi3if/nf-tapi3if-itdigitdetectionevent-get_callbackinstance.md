---
UID: NF:tapi3if.ITDigitDetectionEvent.get_CallbackInstance
title: ITDigitDetectionEvent::get_CallbackInstance (tapi3if.h)
description: The get_CallbackInstance method gets a pointer to the callback instance associated with the event. (ITDigitDetectionEvent.get_CallbackInstance)
helpviewer_keywords: ["ITDigitDetectionEvent interface [TAPI 2.2]","get_CallbackInstance method","ITDigitDetectionEvent.get_CallbackInstance","ITDigitDetectionEvent::get_CallbackInstance","_tapi3_itdigitdetectionevent_get_callbackinstance","get_CallbackInstance","get_CallbackInstance method [TAPI 2.2]","get_CallbackInstance method [TAPI 2.2]","ITDigitDetectionEvent interface","tapi3.itdigitdetectionevent_get_callbackinstance","tapi3if/ITDigitDetectionEvent::get_CallbackInstance"]
old-location: tapi3\itdigitdetectionevent_get_callbackinstance.htm
tech.root: tapi3
ms.assetid: e24d6a37-8f72-42d7-8162-b201eed3cc9a
ms.date: 12/05/2018
ms.keywords: ITDigitDetectionEvent interface [TAPI 2.2],get_CallbackInstance method, ITDigitDetectionEvent.get_CallbackInstance, ITDigitDetectionEvent::get_CallbackInstance, _tapi3_itdigitdetectionevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITDigitDetectionEvent interface, tapi3.itdigitdetectionevent_get_callbackinstance, tapi3if/ITDigitDetectionEvent::get_CallbackInstance
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
 - ITDigitDetectionEvent::get_CallbackInstance
 - tapi3if/ITDigitDetectionEvent::get_CallbackInstance
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
 - ITDigitDetectionEvent.get_CallbackInstance
---

# ITDigitDetectionEvent::get_CallbackInstance


## -description

The 
<b>get_CallbackInstance</b> method gets a pointer to the callback instance associated with the event.

## -parameters

### -param plCallbackInstance [out]

Pointer to the callback instance returned by 
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



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitdetectionevent">ITDigitDetectionEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>
