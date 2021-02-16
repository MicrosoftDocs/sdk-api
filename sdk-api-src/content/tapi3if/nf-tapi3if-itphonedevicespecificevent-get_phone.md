---
UID: NF:tapi3if.ITPhoneDeviceSpecificEvent.get_Phone
title: ITPhoneDeviceSpecificEvent::get_Phone (tapi3if.h)
description: The get_Phone method retrieves the ITPhone interface pointer for a phone device event.
helpviewer_keywords: ["ITPhoneDeviceSpecificEvent interface [TAPI 2.2]","get_Phone method","ITPhoneDeviceSpecificEvent.get_Phone","ITPhoneDeviceSpecificEvent::get_Phone","_tapi3_itphonedevicespecificevent_get_phone","get_Phone","get_Phone method [TAPI 2.2]","get_Phone method [TAPI 2.2]","ITPhoneDeviceSpecificEvent interface","tapi3.itphonedevicespecificevent_get_phone","tapi3if/ITPhoneDeviceSpecificEvent::get_Phone"]
old-location: tapi3\itphonedevicespecificevent_get_phone.htm
tech.root: tapi3
ms.assetid: 068f4172-92a4-41cc-b554-c6e4014505eb
ms.date: 12/05/2018
ms.keywords: ITPhoneDeviceSpecificEvent interface [TAPI 2.2],get_Phone method, ITPhoneDeviceSpecificEvent.get_Phone, ITPhoneDeviceSpecificEvent::get_Phone, _tapi3_itphonedevicespecificevent_get_phone, get_Phone, get_Phone method [TAPI 2.2], get_Phone method [TAPI 2.2],ITPhoneDeviceSpecificEvent interface, tapi3.itphonedevicespecificevent_get_phone, tapi3if/ITPhoneDeviceSpecificEvent::get_Phone
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
 - ITPhoneDeviceSpecificEvent::get_Phone
 - tapi3if/ITPhoneDeviceSpecificEvent::get_Phone
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
 - ITPhoneDeviceSpecificEvent.get_Phone
---

# ITPhoneDeviceSpecificEvent::get_Phone


## -description

The 
<b>get_Phone</b> method retrieves the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface pointer for a phone device event.

## -parameters

### -param ppPhone [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface for the phone object involved in the event.

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
The <i>ppPhone</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphonedevicespecificevent">ITPhoneDeviceSpecificEvent</a>