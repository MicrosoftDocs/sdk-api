---
UID: NF:tapi3if.ITDigitGenerationEvent.get_CallbackInstance
title: ITDigitGenerationEvent::get_CallbackInstance (tapi3if.h)
description: The get_CallbackInstance method gets a pointer to the callback instance associated with the event. (ITDigitGenerationEvent.get_CallbackInstance)
helpviewer_keywords: ["ITDigitGenerationEvent interface [TAPI 2.2]","get_CallbackInstance method","ITDigitGenerationEvent.get_CallbackInstance","ITDigitGenerationEvent::get_CallbackInstance","_tapi3_itdigitgenerationevent_get_callbackinstance","get_CallbackInstance","get_CallbackInstance method [TAPI 2.2]","get_CallbackInstance method [TAPI 2.2]","ITDigitGenerationEvent interface","tapi3.itdigitgenerationevent_get_callbackinstance","tapi3if/ITDigitGenerationEvent::get_CallbackInstance"]
old-location: tapi3\itdigitgenerationevent_get_callbackinstance.htm
tech.root: tapi3
ms.assetid: e0cc1e75-bdc2-4b05-a83b-13e4778ed75b
ms.date: 12/05/2018
ms.keywords: ITDigitGenerationEvent interface [TAPI 2.2],get_CallbackInstance method, ITDigitGenerationEvent.get_CallbackInstance, ITDigitGenerationEvent::get_CallbackInstance, _tapi3_itdigitgenerationevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITDigitGenerationEvent interface, tapi3.itdigitgenerationevent_get_callbackinstance, tapi3if/ITDigitGenerationEvent::get_CallbackInstance
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
 - ITDigitGenerationEvent::get_CallbackInstance
 - tapi3if/ITDigitGenerationEvent::get_CallbackInstance
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
 - ITDigitGenerationEvent.get_CallbackInstance
---

# ITDigitGenerationEvent::get_CallbackInstance


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCallbackInstance</i> parameter is not a valid pointer.

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

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitgenerationevent">ITDigitGenerationEvent</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-registercallnotifications">ITTAPI::RegisterCallNotifications</a>
