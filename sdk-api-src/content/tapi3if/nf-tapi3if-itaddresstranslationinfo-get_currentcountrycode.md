---
UID: NF:tapi3if.ITAddressTranslationInfo.get_CurrentCountryCode
title: ITAddressTranslationInfo::get_CurrentCountryCode (tapi3if.h)
description: The get_CurrentCountryCode method gets the current country/region code.
helpviewer_keywords: ["ITAddressTranslationInfo interface [TAPI 2.2]","get_CurrentCountryCode method","ITAddressTranslationInfo.get_CurrentCountryCode","ITAddressTranslationInfo::get_CurrentCountryCode","_tapi3_itaddresstranslationinfo_get_currentcountrycode","get_CurrentCountryCode","get_CurrentCountryCode method [TAPI 2.2]","get_CurrentCountryCode method [TAPI 2.2]","ITAddressTranslationInfo interface","tapi3.itaddresstranslationinfo_get_currentcountrycode","tapi3if/ITAddressTranslationInfo::get_CurrentCountryCode"]
old-location: tapi3\itaddresstranslationinfo_get_currentcountrycode.htm
tech.root: tapi3
ms.assetid: 02b19558-d7cb-4c77-977b-9810468ff145
ms.date: 12/05/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_CurrentCountryCode method, ITAddressTranslationInfo.get_CurrentCountryCode, ITAddressTranslationInfo::get_CurrentCountryCode, _tapi3_itaddresstranslationinfo_get_currentcountrycode, get_CurrentCountryCode, get_CurrentCountryCode method [TAPI 2.2], get_CurrentCountryCode method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_currentcountrycode, tapi3if/ITAddressTranslationInfo::get_CurrentCountryCode
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
 - ITAddressTranslationInfo::get_CurrentCountryCode
 - tapi3if/ITAddressTranslationInfo::get_CurrentCountryCode
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
 - ITAddressTranslationInfo.get_CurrentCountryCode
---

# ITAddressTranslationInfo::get_CurrentCountryCode


## -description

The 
<b>get_CurrentCountryCode</b> method gets the current country/region code.

## -parameters

### -param CountryCode [out]

Pointer to the country/region code.

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
The <i>CountryCode</i> parameter is not a valid pointer.

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

Corresponds to the <b>dwCurrentCountry</b> member of the TAPI 2 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a> structure.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>