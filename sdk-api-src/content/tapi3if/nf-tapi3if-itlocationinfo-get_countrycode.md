---
UID: NF:tapi3if.ITLocationInfo.get_CountryCode
title: ITLocationInfo::get_CountryCode (tapi3if.h)
description: The get_CountryCode method gets the country/region code.
helpviewer_keywords: ["ITLocationInfo interface [TAPI 2.2]","get_CountryCode method","ITLocationInfo.get_CountryCode","ITLocationInfo::get_CountryCode","_tapi3_itlocationinfo_get_countrycode","get_CountryCode","get_CountryCode method [TAPI 2.2]","get_CountryCode method [TAPI 2.2]","ITLocationInfo interface","tapi3.itlocationinfo_get_countrycode","tapi3if/ITLocationInfo::get_CountryCode"]
old-location: tapi3\itlocationinfo_get_countrycode.htm
tech.root: tapi3
ms.assetid: 3ddd2e25-39ac-419b-9f99-85c6086f0377
ms.date: 12/05/2018
ms.keywords: ITLocationInfo interface [TAPI 2.2],get_CountryCode method, ITLocationInfo.get_CountryCode, ITLocationInfo::get_CountryCode, _tapi3_itlocationinfo_get_countrycode, get_CountryCode, get_CountryCode method [TAPI 2.2], get_CountryCode method [TAPI 2.2],ITLocationInfo interface, tapi3.itlocationinfo_get_countrycode, tapi3if/ITLocationInfo::get_CountryCode
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
 - ITLocationInfo::get_CountryCode
 - tapi3if/ITLocationInfo::get_CountryCode
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
 - ITLocationInfo.get_CountryCode
---

# ITLocationInfo::get_CountryCode


## -description

The 
<b>get_CountryCode</b> method gets the country/region code.

## -parameters

### -param plCountryCode [out]

Pointer to country/region code.

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
The <i>plCountryCode</i> parameter is not a valid pointer.

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

The value that this method returns corresponds to the <b>dwCountryCode</b> member of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a> structure.

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linelocationentry">LINELOCATIONENTRY</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">lineGetTranslateCaps</a>