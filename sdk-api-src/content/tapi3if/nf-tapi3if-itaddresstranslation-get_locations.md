---
UID: NF:tapi3if.ITAddressTranslation.get_Locations
title: ITAddressTranslation::get_Locations (tapi3if.h)
description: The get_Locations method creates a collection of currently available address locations. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the EnumerateLocations method.
helpviewer_keywords: ["ITAddressTranslation interface [TAPI 2.2]","get_Locations method","ITAddressTranslation.get_Locations","ITAddressTranslation::get_Locations","_tapi3_itaddresstranslation_get_locations","get_Locations","get_Locations method [TAPI 2.2]","get_Locations method [TAPI 2.2]","ITAddressTranslation interface","tapi3.itaddresstranslation_get_locations","tapi3if/ITAddressTranslation::get_Locations"]
old-location: tapi3\itaddresstranslation_get_locations.htm
tech.root: tapi3
ms.assetid: b18f7cb1-fcec-41eb-ac57-bf2d47f958e0
ms.date: 12/05/2018
ms.keywords: ITAddressTranslation interface [TAPI 2.2],get_Locations method, ITAddressTranslation.get_Locations, ITAddressTranslation::get_Locations, _tapi3_itaddresstranslation_get_locations, get_Locations, get_Locations method [TAPI 2.2], get_Locations method [TAPI 2.2],ITAddressTranslation interface, tapi3.itaddresstranslation_get_locations, tapi3if/ITAddressTranslation::get_Locations
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
 - ITAddressTranslation::get_Locations
 - tapi3if/ITAddressTranslation::get_Locations
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
 - ITAddressTranslation.get_Locations
---

# ITAddressTranslation::get_Locations


## -description

The 
<b>get_Locations</b> method creates a collection of currently available address locations. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratelocations">EnumerateLocations</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a> interface pointers (location objects).

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
The <i>pVariant</i> parameter is not a valid pointer.

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

The 
<b>get_Locations</b> method is a COM wrapper for the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">LineGetTranslateCaps</a> function, and takes location information from the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure returned by that function.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a> interface returned by <b>ITAddressTranslation::get_Locations</b>. The application must call <b>Release</b> on the 
<b>ITLocationInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratelocations">EnumerateLocations</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo">ITLocationInfo</a>