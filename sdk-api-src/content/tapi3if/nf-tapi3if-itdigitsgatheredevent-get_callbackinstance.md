---
UID: NF:tapi3if.ITDigitsGatheredEvent.get_CallbackInstance
title: ITDigitsGatheredEvent::get_CallbackInstance (tapi3if.h)
description: The get_CallbackInstance method gets a pointer to the application's callback function that will process the event. (ITDigitsGatheredEvent.get_CallbackInstance)
helpviewer_keywords: ["ITDigitsGatheredEvent interface [TAPI 2.2]","get_CallbackInstance method","ITDigitsGatheredEvent.get_CallbackInstance","ITDigitsGatheredEvent::get_CallbackInstance","_tapi3_itdigitsgatheredevent_get_callbackinstance","get_CallbackInstance","get_CallbackInstance method [TAPI 2.2]","get_CallbackInstance method [TAPI 2.2]","ITDigitsGatheredEvent interface","tapi3.itdigitsgatheredevent_get_callbackinstance","tapi3if/ITDigitsGatheredEvent::get_CallbackInstance"]
old-location: tapi3\itdigitsgatheredevent_get_callbackinstance.htm
tech.root: tapi3
ms.assetid: 28c613bc-8320-43b5-a9b3-b6a47876d7dd
ms.date: 12/05/2018
ms.keywords: ITDigitsGatheredEvent interface [TAPI 2.2],get_CallbackInstance method, ITDigitsGatheredEvent.get_CallbackInstance, ITDigitsGatheredEvent::get_CallbackInstance, _tapi3_itdigitsgatheredevent_get_callbackinstance, get_CallbackInstance, get_CallbackInstance method [TAPI 2.2], get_CallbackInstance method [TAPI 2.2],ITDigitsGatheredEvent interface, tapi3.itdigitsgatheredevent_get_callbackinstance, tapi3if/ITDigitsGatheredEvent::get_CallbackInstance
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
 - ITDigitsGatheredEvent::get_CallbackInstance
 - tapi3if/ITDigitsGatheredEvent::get_CallbackInstance
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
 - ITDigitsGatheredEvent.get_CallbackInstance
---

# ITDigitsGatheredEvent::get_CallbackInstance


## -description

The 
<b>get_CallbackInstance</b> method gets a pointer to the application's callback function that will process the event.

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
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itdigitsgatheredevent">ITDigitsGatheredEvent</a>
