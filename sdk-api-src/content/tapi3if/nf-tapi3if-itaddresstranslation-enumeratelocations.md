---
UID: NF:tapi3if.ITAddressTranslation.EnumerateLocations
title: ITAddressTranslation::EnumerateLocations (tapi3if.h)
description: The EnumerateLocations method enumerates the currently available address locations. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the get_Locations method.
helpviewer_keywords: ["EnumerateLocations","EnumerateLocations method [TAPI 2.2]","EnumerateLocations method [TAPI 2.2]","ITAddressTranslation interface","ITAddressTranslation interface [TAPI 2.2]","EnumerateLocations method","ITAddressTranslation.EnumerateLocations","ITAddressTranslation::EnumerateLocations","_tapi3_itaddresstranslation_enumeratelocations","tapi3.itaddresstranslation_enumeratelocations","tapi3if/ITAddressTranslation::EnumerateLocations"]
old-location: tapi3\itaddresstranslation_enumeratelocations.htm
tech.root: tapi3
ms.assetid: b286c738-1037-4a11-8c71-192b050d1502
ms.date: 12/05/2018
ms.keywords: EnumerateLocations, EnumerateLocations method [TAPI 2.2], EnumerateLocations method [TAPI 2.2],ITAddressTranslation interface, ITAddressTranslation interface [TAPI 2.2],EnumerateLocations method, ITAddressTranslation.EnumerateLocations, ITAddressTranslation::EnumerateLocations, _tapi3_itaddresstranslation_enumeratelocations, tapi3.itaddresstranslation_enumeratelocations, tapi3if/ITAddressTranslation::EnumerateLocations
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
 - ITAddressTranslation::EnumerateLocations
 - tapi3if/ITAddressTranslation::EnumerateLocations
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
 - ITAddressTranslation.EnumerateLocations
---

# ITAddressTranslation::EnumerateLocations


## -description

The 
<b>EnumerateLocations</b> method enumerates the currently available address locations. This method is provided for C and C++ applications. Automation client applications, such as those written in Visual Basic, must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-get_locations">get_Locations</a> method.

## -parameters

### -param ppEnumLocation [out]

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumlocation">IEnumLocation</a> object created.

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
The <i>ppEnumLocations</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to create object.

</td>
</tr>
</table>

## -remarks

The 
<b>EnumerateLocations</b> method is a COM wrapper for the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">LineGetTranslateCaps</a> function, and takes location information from the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure returned by that function.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumlocation">IEnumLocation</a> interface returned by <b>ITAddressTranslation::EnumerateLocations</b>. The application must call <b>Release</b> on the 
<b>IEnumLocation</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-ienumlocation">IEnumLocation</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>