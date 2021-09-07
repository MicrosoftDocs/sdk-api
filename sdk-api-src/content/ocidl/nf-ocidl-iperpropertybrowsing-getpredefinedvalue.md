---
UID: NF:ocidl.IPerPropertyBrowsing.GetPredefinedValue
title: IPerPropertyBrowsing::GetPredefinedValue (ocidl.h)
description: Retrieves the value of the specified property that is associated with a predefined string name.
helpviewer_keywords: ["GetPredefinedValue","GetPredefinedValue method [COM]","GetPredefinedValue method [COM]","IPerPropertyBrowsing interface","IPerPropertyBrowsing interface [COM]","GetPredefinedValue method","IPerPropertyBrowsing.GetPredefinedValue","IPerPropertyBrowsing::GetPredefinedValue","_ctrl_iperpropertybrowsing_getpredefinedvalue","com.iperpropertybrowsing_getpredefinedvalue","ocidl/IPerPropertyBrowsing::GetPredefinedValue"]
old-location: com\iperpropertybrowsing_getpredefinedvalue.htm
tech.root: com
ms.assetid: a532ebed-3ed8-4b49-a17f-f542fdbd74ff
ms.date: 12/05/2018
ms.keywords: GetPredefinedValue, GetPredefinedValue method [COM], GetPredefinedValue method [COM],IPerPropertyBrowsing interface, IPerPropertyBrowsing interface [COM],GetPredefinedValue method, IPerPropertyBrowsing.GetPredefinedValue, IPerPropertyBrowsing::GetPredefinedValue, _ctrl_iperpropertybrowsing_getpredefinedvalue, com.iperpropertybrowsing_getpredefinedvalue, ocidl/IPerPropertyBrowsing::GetPredefinedValue
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
 - IPerPropertyBrowsing::GetPredefinedValue
 - ocidl/IPerPropertyBrowsing::GetPredefinedValue
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
 - IPerPropertyBrowsing.GetPredefinedValue
---

# IPerPropertyBrowsing::GetPredefinedValue


## -description

Retrieves the value of the specified property that is associated with a predefined string name. This property is associated with a predefined string name as returned from <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings">IPerPropertyBrowsing::GetPredefinedStrings</a>. The predefined string is identified by a token returned from <b>GetPredefinedStrings</b>.

## -parameters

### -param dispID [in]

The dispatch identifier of the property for which a predefined value is requested.

### -param dwCookie [in]

A token identifying which value to return. The token was previously returned in the <i>pCaCookiesOut</i> array filled by <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings">GetPredefinedStrings</a>.

### -param pVarOut [out]

A pointer to the <b>VARIANT</b> value for the property.

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
This object does not support predefined strings or predefined values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The address in <i>pVarOut</i> is not valid. For example, it may be <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
The caller is responsible for freeing any allocations contained in the <b>VARIANT</b>. Unless the <b>vt</b> member of <b>VARIANT</b> is VT_VARIANT, the caller can free memory using a single call to <b>VariantClear</b>. Otherwise, the caller must recursively free the contained <b>VARIANT</b> values before freeing the outer <b>VARIANT</b>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
Support for predefined names and values is not required. If your object does not support these names, return E_NOTIMPL from this method. If this method is not implemented, <a href="/windows/desktop/api/ocidl/nf-ocidl-iperpropertybrowsing-getpredefinedstrings">IPerPropertyBrowsing::GetPredefinedStrings</a> must not be implemented either.

This method allocates any memory needed inside the <b>VARIANT</b>.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-iperpropertybrowsing">IPerPropertyBrowsing</a>