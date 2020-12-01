---
UID: NF:tapi3if.ITAddressTranslationInfo.get_DestinationCountryCode
title: ITAddressTranslationInfo::get_DestinationCountryCode (tapi3if.h)
description: Retrieves the country/region code for the call destination.
helpviewer_keywords: ["ITAddressTranslationInfo interface [TAPI 2.2]","get_DestinationCountryCode method","ITAddressTranslationInfo.get_DestinationCountryCode","ITAddressTranslationInfo::get_DestinationCountryCode","_tapi3_itaddresstranslationinfo_get_destinationcountrycode","get_DestinationCountryCode","get_DestinationCountryCode method [TAPI 2.2]","get_DestinationCountryCode method [TAPI 2.2]","ITAddressTranslationInfo interface","tapi3.itaddresstranslationinfo_get_destinationcountrycode","tapi3if/ITAddressTranslationInfo::get_DestinationCountryCode"]
old-location: tapi3\itaddresstranslationinfo_get_destinationcountrycode.htm
tech.root: tapi3
ms.assetid: 29880773-ce19-489f-81d8-d2c91779350f
ms.date: 12/05/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_DestinationCountryCode method, ITAddressTranslationInfo.get_DestinationCountryCode, ITAddressTranslationInfo::get_DestinationCountryCode, _tapi3_itaddresstranslationinfo_get_destinationcountrycode, get_DestinationCountryCode, get_DestinationCountryCode method [TAPI 2.2], get_DestinationCountryCode method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_destinationcountrycode, tapi3if/ITAddressTranslationInfo::get_DestinationCountryCode
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
 - ITAddressTranslationInfo::get_DestinationCountryCode
 - tapi3if/ITAddressTranslationInfo::get_DestinationCountryCode
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
 - ITAddressTranslationInfo.get_DestinationCountryCode
---

# ITAddressTranslationInfo::get_DestinationCountryCode


## -description

The 
<b>get_DestinationCountryCode</b> method retrieves the country/region code for the call destination.

## -parameters

### -param CountryCode [out]

A pointer to destination country/region code.

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
The <i>CountryCode</i> parameter is an invalid pointer.

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

Corresponds to the <b>dwDestCountry</b> member of the TAPI 2 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a> structure.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>