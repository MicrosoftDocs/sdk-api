---
UID: NF:tapi3if.ITTAPIObjectEvent.get_Event
title: ITTAPIObjectEvent::get_Event (tapi3if.h)
description: The get_Event method gets information concerning an asynchronous event notification. The application uses TAPIOBJECT_EVENT to determine what type of event is being signaled.
helpviewer_keywords: ["ITTAPIObjectEvent interface [TAPI 2.2]","get_Event method","ITTAPIObjectEvent.get_Event","ITTAPIObjectEvent::get_Event","_tapi3_ittapiobjectevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITTAPIObjectEvent interface","tapi3.ittapiobjectevent_get_event","tapi3if/ITTAPIObjectEvent::get_Event"]
old-location: tapi3\ittapiobjectevent_get_event.htm
tech.root: tapi3
ms.assetid: 5ae4362f-6987-461e-928f-9478e37e0380
ms.date: 12/05/2018
ms.keywords: ITTAPIObjectEvent interface [TAPI 2.2],get_Event method, ITTAPIObjectEvent.get_Event, ITTAPIObjectEvent::get_Event, _tapi3_ittapiobjectevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITTAPIObjectEvent interface, tapi3.ittapiobjectevent_get_event, tapi3if/ITTAPIObjectEvent::get_Event
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
 - ITTAPIObjectEvent::get_Event
 - tapi3if/ITTAPIObjectEvent::get_Event
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
 - ITTAPIObjectEvent.get_Event
---

# ITTAPIObjectEvent::get_Event


## -description

The 
<b>get_Event</b> method gets information concerning an asynchronous event notification. The application uses 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapiobject_event">TAPIOBJECT_EVENT</a> to determine what type of event is being signaled.

## -parameters

### -param pEvent [out]

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapiobject_event">TAPIOBJECT_EVENT</a> indicator of the event.

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

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ittapiobjectevent">ITTAPIObjectEvent</a>



<a href="/windows/desktop/Tapi/tapi-object">TAPI Object</a>



<a href="/windows/desktop/api/tapi3if/ne-tapi3if-tapiobject_event">TAPIOBJECT_EVENT</a>