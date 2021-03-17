---
UID: NF:tapi3if.ITAddressDeviceSpecificEvent.get_Address
title: ITAddressDeviceSpecificEvent::get_Address (tapi3if.h)
description: The get_Address method gets a pointer to the ITAddress interface of the Address object involved in the event.
helpviewer_keywords: ["ITAddressDeviceSpecificEvent interface [TAPI 2.2]","get_Address method","ITAddressDeviceSpecificEvent.get_Address","ITAddressDeviceSpecificEvent::get_Address","_tapi3_itaddressdevicespecificevent_get_address","get_Address","get_Address method [TAPI 2.2]","get_Address method [TAPI 2.2]","ITAddressDeviceSpecificEvent interface","tapi3.itaddressdevicespecificevent_get_address","tapi3if/ITAddressDeviceSpecificEvent::get_Address"]
old-location: tapi3\itaddressdevicespecificevent_get_address.htm
tech.root: tapi3
ms.assetid: 95b745c9-c18a-47c9-8ceb-b2c225ebbf73
ms.date: 12/05/2018
ms.keywords: ITAddressDeviceSpecificEvent interface [TAPI 2.2],get_Address method, ITAddressDeviceSpecificEvent.get_Address, ITAddressDeviceSpecificEvent::get_Address, _tapi3_itaddressdevicespecificevent_get_address, get_Address, get_Address method [TAPI 2.2], get_Address method [TAPI 2.2],ITAddressDeviceSpecificEvent interface, tapi3.itaddressdevicespecificevent_get_address, tapi3if/ITAddressDeviceSpecificEvent::get_Address
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
 - ITAddressDeviceSpecificEvent::get_Address
 - tapi3if/ITAddressDeviceSpecificEvent::get_Address
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
 - ITAddressDeviceSpecificEvent.get_Address
---

# ITAddressDeviceSpecificEvent::get_Address


## -description

The 
<b>get_Address</b> method gets a pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface of the 
<a href="/windows/desktop/Tapi/address-object">Address object</a> involved in the event.

## -parameters

### -param ppAddress [out]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface.

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
The <i>ppAddress</i> parameter is not a valid pointer.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddressdevicespecificevent">ITAddressDeviceSpecificEvent</a>