---
UID: NF:tapi3if.ITAddressTranslationInfo.get_DialableString
title: ITAddressTranslationInfo::get_DialableString (tapi3if.h)
description: The get_DialableString method gets a string that contains a dialable number. Typically, this number is then used as the pDestAddress argument in ITAddress::CreateCall.
helpviewer_keywords: ["ITAddressTranslationInfo interface [TAPI 2.2]","get_DialableString method","ITAddressTranslationInfo.get_DialableString","ITAddressTranslationInfo::get_DialableString","_tapi3_itaddresstranslationinfo_get_dialablestring","get_DialableString","get_DialableString method [TAPI 2.2]","get_DialableString method [TAPI 2.2]","ITAddressTranslationInfo interface","tapi3.itaddresstranslationinfo_get_dialablestring","tapi3if/ITAddressTranslationInfo::get_DialableString"]
old-location: tapi3\itaddresstranslationinfo_get_dialablestring.htm
tech.root: tapi3
ms.assetid: 76177de9-eab2-4a86-ac25-29b78606b854
ms.date: 12/05/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_DialableString method, ITAddressTranslationInfo.get_DialableString, ITAddressTranslationInfo::get_DialableString, _tapi3_itaddresstranslationinfo_get_dialablestring, get_DialableString, get_DialableString method [TAPI 2.2], get_DialableString method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_dialablestring, tapi3if/ITAddressTranslationInfo::get_DialableString
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
 - ITAddressTranslationInfo::get_DialableString
 - tapi3if/ITAddressTranslationInfo::get_DialableString
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
 - ITAddressTranslationInfo.get_DialableString
---

# ITAddressTranslationInfo::get_DialableString


## -description

The 
<b>get_DialableString</b> method gets a string that contains a dialable number. Typically, this number is then used as the <i>pDestAddress</i> argument in 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a>.

## -parameters

### -param ppDialableString [out]

Pointer to <b>BSTR</b> containing representation of dialable string.

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
The <i>ppDialableString</i> parameter is not a valid pointer.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppDialableString</i> parameter.
			

Corresponds to the <b>dwDialableStringSize</b> and <b>dwDialableStringOffset</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a> structure.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>