---
UID: NF:tapi3if.ITAddress.get_ServiceProviderName
title: ITAddress::get_ServiceProviderName (tapi3if.h)
description: The get_ServiceProviderName method gets the name of the Telephony Service Provider (TSP) that supports this address:\_for example, Unimdm.tsp for the Unimodem service provider or H323.tsp for the H323 service provider.
helpviewer_keywords: ["ITAddress interface [TAPI 2.2]","get_ServiceProviderName method","ITAddress.get_ServiceProviderName","ITAddress::get_ServiceProviderName","_tapi3_itaddress_get_serviceprovidername","get_ServiceProviderName","get_ServiceProviderName method [TAPI 2.2]","get_ServiceProviderName method [TAPI 2.2]","ITAddress interface","tapi3.itaddress_get_serviceprovidername","tapi3if/ITAddress::get_ServiceProviderName"]
old-location: tapi3\itaddress_get_serviceprovidername.htm
tech.root: tapi3
ms.assetid: fa49d256-58e0-4d7e-a121-387a3a704519
ms.date: 12/05/2018
ms.keywords: ITAddress interface [TAPI 2.2],get_ServiceProviderName method, ITAddress.get_ServiceProviderName, ITAddress::get_ServiceProviderName, _tapi3_itaddress_get_serviceprovidername, get_ServiceProviderName, get_ServiceProviderName method [TAPI 2.2], get_ServiceProviderName method [TAPI 2.2],ITAddress interface, tapi3.itaddress_get_serviceprovidername, tapi3if/ITAddress::get_ServiceProviderName
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
 - ITAddress::get_ServiceProviderName
 - tapi3if/ITAddress::get_ServiceProviderName
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
 - ITAddress.get_ServiceProviderName
---

# ITAddress::get_ServiceProviderName


## -description

The 
<b>get_ServiceProviderName</b> method gets the name of the Telephony Service Provider (TSP) that supports this address: for example, Unimdm.tsp for the Unimodem service provider or H323.tsp for the H323 service provider.

## -parameters

### -param ppName [out]

Pointer to <b>BSTR</b> containing the service provider name.

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
The <i>ppName</i> parameter is not a valid pointer.

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
<dt><b>TAPI_E_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
No service provider was found that supports the current address.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppName</i> parameter.
			

You can retrieve the name of the provider in a TSP-dependent format using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapabilitystring">ITAddressCapabilities::get_AddressCapabilityString</a> with <i>AddressCapString</i> set to ACS_PROVIDERSPECIFIC, which returns the string found in the <b>dwProviderInfoOffset</b> member of the TAPI 2.<i>x</i>
<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a> structure.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresscapabilities-get_addresscapabilitystring">ITAddressCapabilities::get_AddressCapabilityString</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linedevcaps">LINEDEVCAPS</a>