---
UID: NF:ocidl.IPerPropertyBrowsing.GetPredefinedStrings
title: IPerPropertyBrowsing::GetPredefinedStrings (ocidl.h)
description: Retrieves an array description strings for the allowable values that the specified property can accept.
helpviewer_keywords: ["GetPredefinedStrings","GetPredefinedStrings method [COM]","GetPredefinedStrings method [COM]","IPerPropertyBrowsing interface","IPerPropertyBrowsing interface [COM]","GetPredefinedStrings method","IPerPropertyBrowsing.GetPredefinedStrings","IPerPropertyBrowsing::GetPredefinedStrings","_ctrl_iperpropertybrowsing_getpredefinedstrings","com.iperpropertybrowsing_getpredefinedstrings","ocidl/IPerPropertyBrowsing::GetPredefinedStrings"]
old-location: com\iperpropertybrowsing_getpredefinedstrings.htm
tech.root: com
ms.assetid: 1b20585f-2bcd-475e-abee-80158692ae0f
ms.date: 12/05/2018
ms.keywords: GetPredefinedStrings, GetPredefinedStrings method [COM], GetPredefinedStrings method [COM],IPerPropertyBrowsing interface, IPerPropertyBrowsing interface [COM],GetPredefinedStrings method, IPerPropertyBrowsing.GetPredefinedStrings, IPerPropertyBrowsing::GetPredefinedStrings, _ctrl_iperpropertybrowsing_getpredefinedstrings, com.iperpropertybrowsing_getpredefinedstrings, ocidl/IPerPropertyBrowsing::GetPredefinedStrings
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPerPropertyBrowsing::GetPredefinedStrings
 - ocidl/IPerPropertyBrowsing::GetPredefinedStrings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPerPropertyBrowsing.GetPredefinedStrings
---

# IPerPropertyBrowsing::GetPredefinedStrings


## -description

Retrieves an array description strings for the allowable values that the specified property can accept.

## -parameters

### -param dispID [in]

The dispatch identifier of the property.

### -param pCaStringsOut [out]

A pointer to a caller-allocated, counted array structure that contains the element count and address of a method-allocated array of string pointers. This method also allocates memory for the string values containing the predefined names, and it stores the string pointers in the array. If the method fails, no memory is allocated, and the contents of the structure are undefined.

### -param pCaCookiesOut [out]

A pointer to the caller-allocated, counted array structure that contains the element count and address of a method-allocated array of <b>DWORD</b> values. The values in the array can be passed to <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue">IPerPropertyBrowsing::GetPredefinedValue</a> to retrieve the value associated with the name in the same array position inside <i>pCaStringsOut</i>. If the method fails, no memory is allocated, and the contents of the structure are undefined.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented and predefined names are not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pCaStringsOut</i> or <i>pCaCookiesOut</i> is not valid. For example, either parameter may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

Each string returned in the array pointed to by <i>pCaStringsOut</i> has a matching token in the counted array pointed to by <i>pCaCookiesOut</i>, where the token can be passed to <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue">IPerPropertyBrowsing::GetPredefinedValue</a> to get the actual value (a <b>VARIANT</b>) corresponding to the string.

Using the predefined strings, a caller can obtain a list of strings for populating user interface elements, such as a drop-down listbox. When the end user selects one of these strings as a value to assign to a property, the caller can then obtain the corresponding value through <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue">IPerPropertyBrowsing::GetPredefinedValue</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Both the <a href="/windows/desktop/api/ocidl/ns-ocidl-calpolestr">CALPOLESTR</a> and <a href="/windows/desktop/api/ocidl/ns-ocidl-cadword">CADWORD</a> structures passed to this method are caller-allocated. The caller is responsible for freeing each string pointed to from the <b>CALPOLESTR</b> array as well as the <b>CALPOLESTR</b> structure.

All memory is allocated with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. The caller is responsible for freeing the strings and the array with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

Upon return from this method, the caller is responsible for all this memory and must free it when it is no longer needed. Code to achieve this appears as follows.


``` syntax
CALPOLESTR     castr; 
CWDWORD        cadw; 
ULONG          i; 
 
pIPerPropertyBrowsing->GetPredefinedStrings(dispID, &castr, &cadw); 
 
//...Use the strings and the cookies 
 
CoTaskMemFree((void *)cadw.pElems); 
 
for (i=0; i < castr.cElems; i++) 
    CoTaskMemFree((void *)castr.pElems[i]); 
 
CoTaskMemFree((void *)castr.pElems); 

```

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Support for predefined names and values is not required. If your object does not support these names, return E_NOTIMPL from this method. If this method is not implemented, <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedvalue">IPerPropertyBrowsing::GetPredefinedValue</a> must not be implemented either.

This method fills the <b>cElems</b> and <b>pElems</b> members of the <a href="/windows/desktop/api/ocidl/ns-ocidl-cadword">CADWORD</a> and <a href="/windows/desktop/api/ocidl/ns-ocidl-calpolestr">CALPOLESTR</a> structures. It allocates the arrays pointed to by these structures with <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> and fills those arrays. In the <b>CALPOLESTR</b> case, this method also allocates each string with <b>CoTaskMemAlloc</b>, storing each string pointer in the array.

## -see-also

<a href="/windows/desktop/api/ocidl/ns-ocidl-cadword">CADWORD</a>



<a href="/windows/desktop/api/ocidl/ns-ocidl-calpolestr">CALPOLESTR</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>
