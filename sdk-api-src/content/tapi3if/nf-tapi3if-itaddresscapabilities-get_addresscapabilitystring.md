---
UID: NF:tapi3if.ITAddressCapabilities.get_AddressCapabilityString
title: ITAddressCapabilities::get_AddressCapabilityString (tapi3if.h)
description: The get_AddressCapabilityString method gets the capability string for a given ADDRESS_CAPABILITY_STRING.
helpviewer_keywords: ["ITAddressCapabilities interface [TAPI 2.2]","get_AddressCapabilityString method","ITAddressCapabilities.get_AddressCapabilityString","ITAddressCapabilities::get_AddressCapabilityString","_tapi3_itaddresscapabilities_get_addresscapabilitystring","get_AddressCapabilityString","get_AddressCapabilityString method [TAPI 2.2]","get_AddressCapabilityString method [TAPI 2.2]","ITAddressCapabilities interface","tapi3.itaddresscapabilities_get_addresscapabilitystring","tapi3if/ITAddressCapabilities::get_AddressCapabilityString"]
old-location: tapi3\itaddresscapabilities_get_addresscapabilitystring.htm
tech.root: tapi3
ms.assetid: 9ec4c25e-700b-4aed-97ff-e7cb420fdf96
ms.date: 12/05/2018
ms.keywords: ITAddressCapabilities interface [TAPI 2.2],get_AddressCapabilityString method, ITAddressCapabilities.get_AddressCapabilityString, ITAddressCapabilities::get_AddressCapabilityString, _tapi3_itaddresscapabilities_get_addresscapabilitystring, get_AddressCapabilityString, get_AddressCapabilityString method [TAPI 2.2], get_AddressCapabilityString method [TAPI 2.2],ITAddressCapabilities interface, tapi3.itaddresscapabilities_get_addresscapabilitystring, tapi3if/ITAddressCapabilities::get_AddressCapabilityString
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
 - ITAddressCapabilities::get_AddressCapabilityString
 - tapi3if/ITAddressCapabilities::get_AddressCapabilityString
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
 - ITAddressCapabilities.get_AddressCapabilityString
---

# ITAddressCapabilities::get_AddressCapabilityString


## -description

The 
<b>get_AddressCapabilityString</b> method gets the capability string for a given 
<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_capability_string">ADDRESS_CAPABILITY_STRING</a>.

## -parameters

### -param AddressCapString [in]

Descriptor for desired address capability string.

### -param ppCapabilityString [out]

Pointer to <b>BSTR</b> value of address capability. <b>NULL</b> is a possible return value if the TSP does not provide a value for <i>AddressCapString</i>.

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
The <i>AddressCapString</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppCapabilityString</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NOTSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
TAPI version is not 3.0 or higher.

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

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppCapabilityString</i> parameter.

## -see-also

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-address_capability_string">ADDRESS_CAPABILITY_STRING</a>



<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities">ITAddressCapabilities</a>