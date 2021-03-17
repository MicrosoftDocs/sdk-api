---
UID: NF:tapi3if.ITAddressTranslation.TranslateAddress
title: ITAddressTranslation::TranslateAddress (tapi3if.h)
description: The TranslateAddress method creates the address translation information interface.
helpviewer_keywords: ["ITAddressTranslation interface [TAPI 2.2]","TranslateAddress method","ITAddressTranslation.TranslateAddress","ITAddressTranslation::TranslateAddress","TranslateAddress","TranslateAddress method [TAPI 2.2]","TranslateAddress method [TAPI 2.2]","ITAddressTranslation interface","_tapi3_itaddresstranslation_translateaddress","tapi3.itaddresstranslation_translateaddress","tapi3if/ITAddressTranslation::TranslateAddress"]
old-location: tapi3\itaddresstranslation_translateaddress.htm
tech.root: tapi3
ms.assetid: 14e51de8-33fd-4de0-bc1c-5f8085ea095c
ms.date: 12/05/2018
ms.keywords: ITAddressTranslation interface [TAPI 2.2],TranslateAddress method, ITAddressTranslation.TranslateAddress, ITAddressTranslation::TranslateAddress, TranslateAddress, TranslateAddress method [TAPI 2.2], TranslateAddress method [TAPI 2.2],ITAddressTranslation interface, _tapi3_itaddresstranslation_translateaddress, tapi3.itaddresstranslation_translateaddress, tapi3if/ITAddressTranslation::TranslateAddress
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
 - ITAddressTranslation::TranslateAddress
 - tapi3if/ITAddressTranslation::TranslateAddress
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
 - ITAddressTranslation.TranslateAddress
---

# ITAddressTranslation::TranslateAddress


## -description

The 
<b>TranslateAddress</b> method creates the address translation information interface. The primary goal of the 
<b>TranslateAddress</b> method is to obtain the <i>pDestAddress</i> string (<a href="/windows/desktop/Tapi/address-ovr">dialable address</a>) needed as a parameter for 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>. The 
<b>TranslateAddress</b> method returns the dialable address indirectly, as one of the properties of an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a> object.

## -parameters

### -param pAddressToTranslate [in]

Pointer to <b>BSTR</b> containing address that requires translation.

### -param lCard [in]

Calling card used for translation.

### -param lTranslateOptions [in]

Indicator of translation options, see 
<a href="/windows/desktop/Tapi/linetranslateoption--constants">LINETRANSLATEOPTION__Constants</a>.

### -param ppTranslated [out]

Pointer to newly created 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a> interface.

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
The <i>ppTranslated</i> parameter is not a valid pointer.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for unknown reasons.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>lTranslateOptions</i> value is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_NODRIVER</b></dt>
</dl>
</td>
<td width="60%">
This address has no TSP associated with it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_REGISTRY_SETTING_CORRUPT</b></dt>
</dl>
</td>
<td width="60%">
The registry is corrupt.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_OPERATIONFAILED</b></dt>
</dl>
</td>
<td width="60%">
The method failed with TAPI.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_RESOURCEUNAVAIL</b></dt>
</dl>
</td>
<td width="60%">
The TSP is not available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TAPI_E_INVALCARD</b></dt>
</dl>
</td>
<td width="60%">
The card number is not valid.

</td>
</tr>
</table>

## -remarks

The application must use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring">SysAllocString</a> to allocate memory for <i>pAddressToTranslate</i> and use 
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory when the variable is no longer needed.

The 
<b>TranslateAddress</b> method is a COM wrapper for the TAPI 2.1 
<a href="/windows/desktop/api/tapi/nf-tapi-linetranslateaddress">LineTranslateAddress</a> function.

TAPI calls the <b>AddRef</b> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a> interface returned by <b>TranslateAddress</b>. The application must call <b>Release</b> on the 
<b>ITAddressTranslationInfo</b> interface to free resources associated with it.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/Tapi/address-ovr">Dialable Addresses</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation">ITAddressTranslation</a>