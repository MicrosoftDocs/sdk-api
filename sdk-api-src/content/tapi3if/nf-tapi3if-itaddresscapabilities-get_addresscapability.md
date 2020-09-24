---
UID: NF:tapi3if.ITAddressCapabilities.get_AddressCapability
title: ITAddressCapabilities::get_AddressCapability (tapi3if.h)
description: The get_AddressCapability method gets the capability value for a given ADDRESS_CAPABILITY.
helpviewer_keywords: ["ITAddressCapabilities interface [TAPI 2.2]","get_AddressCapability method","ITAddressCapabilities.get_AddressCapability","ITAddressCapabilities::get_AddressCapability","_tapi3_itaddresscapabilities_get_addresscapability","get_AddressCapability","get_AddressCapability method [TAPI 2.2]","get_AddressCapability method [TAPI 2.2]","ITAddressCapabilities interface","tapi3.itaddresscapabilities_get_addresscapability","tapi3if/ITAddressCapabilities::get_AddressCapability"]
old-location: tapi3\itaddresscapabilities_get_addresscapability.htm
tech.root: tapi3
ms.assetid: 76e61d5e-48b6-4b9c-9076-bd20a794859c
ms.date: 12/05/2018
ms.keywords: ITAddressCapabilities interface [TAPI 2.2],get_AddressCapability method, ITAddressCapabilities.get_AddressCapability, ITAddressCapabilities::get_AddressCapability, _tapi3_itaddresscapabilities_get_addresscapability, get_AddressCapability, get_AddressCapability method [TAPI 2.2], get_AddressCapability method [TAPI 2.2],ITAddressCapabilities interface, tapi3.itaddresscapabilities_get_addresscapability, tapi3if/ITAddressCapabilities::get_AddressCapability
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
 - ITAddressCapabilities::get_AddressCapability
 - tapi3if/ITAddressCapabilities::get_AddressCapability
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
 - ITAddressCapabilities.get_AddressCapability
---

# ITAddressCapabilities::get_AddressCapability


## -description

The 
<b>get_AddressCapability</b> method gets the capability value for a given 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_capability">ADDRESS_CAPABILITY</a>.

## -parameters

### -param AddressCap [in]

Descriptor for desired address capability.

### -param plCapability [out]

Value of address capability.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>AddressCap</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>plCapability</i> parameter in not a valid pointer.

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

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_capability">ADDRESS_CAPABILITY</a>



<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities">ITAddressCapabilities</a>