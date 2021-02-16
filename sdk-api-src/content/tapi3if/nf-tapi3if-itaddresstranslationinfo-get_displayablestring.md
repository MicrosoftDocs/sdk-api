---
UID: NF:tapi3if.ITAddressTranslationInfo.get_DisplayableString
title: ITAddressTranslationInfo::get_DisplayableString (tapi3if.h)
description: The get_DisplayableString method gets a string that contains a displayable version of the dialable number.
helpviewer_keywords: ["ITAddressTranslationInfo interface [TAPI 2.2]","get_DisplayableString method","ITAddressTranslationInfo.get_DisplayableString","ITAddressTranslationInfo::get_DisplayableString","_tapi3_itaddresstranslationinfo_get_displayablestring","get_DisplayableString","get_DisplayableString method [TAPI 2.2]","get_DisplayableString method [TAPI 2.2]","ITAddressTranslationInfo interface","tapi3.itaddresstranslationinfo_get_displayablestring","tapi3if/ITAddressTranslationInfo::get_DisplayableString"]
old-location: tapi3\itaddresstranslationinfo_get_displayablestring.htm
tech.root: tapi3
ms.assetid: c88474ee-5a7e-4966-8dc2-5f839069b2d2
ms.date: 12/05/2018
ms.keywords: ITAddressTranslationInfo interface [TAPI 2.2],get_DisplayableString method, ITAddressTranslationInfo.get_DisplayableString, ITAddressTranslationInfo::get_DisplayableString, _tapi3_itaddresstranslationinfo_get_displayablestring, get_DisplayableString, get_DisplayableString method [TAPI 2.2], get_DisplayableString method [TAPI 2.2],ITAddressTranslationInfo interface, tapi3.itaddresstranslationinfo_get_displayablestring, tapi3if/ITAddressTranslationInfo::get_DisplayableString
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
 - ITAddressTranslationInfo::get_DisplayableString
 - tapi3if/ITAddressTranslationInfo::get_DisplayableString
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
 - ITAddressTranslationInfo.get_DisplayableString
---

# ITAddressTranslationInfo::get_DisplayableString


## -description

The 
<b>get_DisplayableString</b> method gets a string that contains a displayable version of the dialable number.

## -parameters

### -param ppDisplayableString [out]

Pointer to <b>BSTR</b> containing representation of displayable string.

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
The <i>ppDisplayableString</i> parameter is not a valid pointer.

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
<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> to free the memory allocated for the <i>ppDisplayableString</i> parameter.
			

Corresponds to the <b>dwDisplayableStringSize</b> and <b>dwDisplayableStringOffset</b> members of TAPI 2's 
<a href="/windows/desktop/api/tapi/ns-tapi-linetranslateoutput">LINETRANSLATEOUTPUT</a> structure.

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo">ITAddressTranslationInfo</a>