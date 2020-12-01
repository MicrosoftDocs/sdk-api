---
UID: NF:tapi3if.ITAddressEvent.get_Event
title: ITAddressEvent::get_Event (tapi3if.h)
description: The get_Event method gets the ADDRESS_EVENT descriptor of an event.
helpviewer_keywords: ["ITAddressEvent interface [TAPI 2.2]","get_Event method","ITAddressEvent.get_Event","ITAddressEvent::get_Event","_tapi3_itaddressevent_get_event","get_Event","get_Event method [TAPI 2.2]","get_Event method [TAPI 2.2]","ITAddressEvent interface","tapi3.itaddressevent_get_event","tapi3if/ITAddressEvent::get_Event"]
old-location: tapi3\itaddressevent_get_event.htm
tech.root: tapi3
ms.assetid: 46dc4ce8-2453-47bb-a101-d925c9317b90
ms.date: 12/05/2018
ms.keywords: ITAddressEvent interface [TAPI 2.2],get_Event method, ITAddressEvent.get_Event, ITAddressEvent::get_Event, _tapi3_itaddressevent_get_event, get_Event, get_Event method [TAPI 2.2], get_Event method [TAPI 2.2],ITAddressEvent interface, tapi3.itaddressevent_get_event, tapi3if/ITAddressEvent::get_Event
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
 - ITAddressEvent::get_Event
 - tapi3if/ITAddressEvent::get_Event
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
 - ITAddressEvent.get_Event
---

# ITAddressEvent::get_Event


## -description

The 
<b>get_Event</b> method gets the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_event">ADDRESS_EVENT</a> descriptor of an event.

## -parameters

### -param pEvent [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_event">ADDRESS_EVENT</a> descriptor of an event.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pEvent</i> parameter is not valid.

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
The <i>pEvent</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -remarks

Certain events on PnP devices, such as AE_NEWTERMINAL and AE_REMOVETERMINAL, will not be received until after the first time static terminals are enumerated using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-enumeratestaticterminals">ITTerminalSupport::EnumerateStaticTerminals</a> or 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-get_staticterminals">ITTerminalSupport::get_StaticTerminals</a>.

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_event">ADDRESS_EVENT</a>



<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent">ITAddressEvent</a>