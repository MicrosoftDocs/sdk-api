---
UID: NF:tapi3if.ITAddressTranslation.get_CallingCards
title: ITAddressTranslation::get_CallingCards (tapi3if.h)
description: The get_CallingCards method creates a collection of calling cards associated with the address.
helpviewer_keywords: ["ITAddressTranslation interface [TAPI 2.2]","get_CallingCards method","ITAddressTranslation.get_CallingCards","ITAddressTranslation::get_CallingCards","_tapi3_itaddresstranslation_get_callingcards","get_CallingCards","get_CallingCards method [TAPI 2.2]","get_CallingCards method [TAPI 2.2]","ITAddressTranslation interface","tapi3.itaddresstranslation_get_callingcards","tapi3if/ITAddressTranslation::get_CallingCards"]
old-location: tapi3\itaddresstranslation_get_callingcards.htm
tech.root: tapi3
ms.assetid: 3033c584-1a7b-4bba-a8a2-2a2d59247689
ms.date: 12/05/2018
ms.keywords: ITAddressTranslation interface [TAPI 2.2],get_CallingCards method, ITAddressTranslation.get_CallingCards, ITAddressTranslation::get_CallingCards, _tapi3_itaddresstranslation_get_callingcards, get_CallingCards, get_CallingCards method [TAPI 2.2], get_CallingCards method [TAPI 2.2],ITAddressTranslation interface, tapi3.itaddresstranslation_get_callingcards, tapi3if/ITAddressTranslation::get_CallingCards
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
 - ITAddressTranslation::get_CallingCards
 - tapi3if/ITAddressTranslation::get_CallingCards
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
 - ITAddressTranslation.get_CallingCards
---

# ITAddressTranslation::get_CallingCards


## -description

The 
<b>get_CallingCards</b> method creates a collection of calling cards associated with the address. This method is provided for Automation client applications, such as those written in Visual Basic. C and C++ applications must use the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddresstranslation-enumeratecallingcards">EnumerateCallingCards</a> method.

## -parameters

### -param pVariant [out]

Pointer to <b>VARIANT</b> containing an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a> of 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard">ITCallingCard</a> interface pointers.

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
<b>get_CallingCards</b> method is a COM wrapper for the TAPI 2.2 
<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">LineGetTranslateCaps</a> function, and takes calling card information from the 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a> structure returned by that function.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard">ITCallingCard</a> interface returned by <b>ITAddressTranslation::get_CallingCards</b>. The application must call <b>Release</b> on the 
<b>ITCallingCard</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard">ITCallingCard</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcollection">ITCollection</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linetranslatecaps">LINETRANSLATECAPS</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegettranslatecaps">LineGetTranslateCaps</a>