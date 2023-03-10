---
UID: NF:msctf.ITfReadOnlyProperty.GetType
title: ITfReadOnlyProperty::GetType (msctf.h)
description: ITfReadOnlyProperty::GetType method
helpviewer_keywords: ["GUID_TFCAT_PROPSTYLE_CUSTOM","GUID_TFCAT_PROPSTYLE_STATIC","GUID_TFCAT_PROPSTYLE_STATICCOMPACT","GetType","GetType method [Text Services Framework]","GetType method [Text Services Framework]","ITfReadOnlyProperty interface","ITfReadOnlyProperty interface [Text Services Framework]","GetType method","ITfReadOnlyProperty.GetType","ITfReadOnlyProperty::GetType","_tsf_itfreadonlyproperty_gettype_ref","msctf/ITfReadOnlyProperty::GetType","tsf.itfreadonlyproperty_gettype"]
old-location: tsf\itfreadonlyproperty_gettype.htm
tech.root: TSF
ms.assetid: a0c47d13-c290-4efe-ad73-6dcb654dc18f
ms.date: 12/05/2018
ms.keywords: GUID_TFCAT_PROPSTYLE_CUSTOM, GUID_TFCAT_PROPSTYLE_STATIC, GUID_TFCAT_PROPSTYLE_STATICCOMPACT, GetType, GetType method [Text Services Framework], GetType method [Text Services Framework],ITfReadOnlyProperty interface, ITfReadOnlyProperty interface [Text Services Framework],GetType method, ITfReadOnlyProperty.GetType, ITfReadOnlyProperty::GetType, _tsf_itfreadonlyproperty_gettype_ref, msctf/ITfReadOnlyProperty::GetType, tsf.itfreadonlyproperty_gettype
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfReadOnlyProperty::GetType
 - msctf/ITfReadOnlyProperty::GetType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfReadOnlyProperty.GetType
---

# ITfReadOnlyProperty::GetType


## -description

Obtains the property identifier.

## -parameters

### -param pguid [out]

Pointer to a <b>GUID</b> value that receives the property type identifier. This is the value that the property provider passed to <a href="/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory</a> when the property was registered. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GUID_TFCAT_PROPSTYLE_STATIC"></a><a id="guid_tfcat_propstyle_static"></a><dl>
<dt><b>GUID_TFCAT_PROPSTYLE_STATIC</b></dt>
</dl>
</td>
<td width="60%">
The property is a static property.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TFCAT_PROPSTYLE_STATICCOMPACT"></a><a id="guid_tfcat_propstyle_staticcompact"></a><dl>
<dt><b>GUID_TFCAT_PROPSTYLE_STATICCOMPACT</b></dt>
</dl>
</td>
<td width="60%">
The property is a static-compact property.

</td>
</tr>
<tr>
<td width="40%"><a id="GUID_TFCAT_PROPSTYLE_CUSTOM"></a><a id="guid_tfcat_propstyle_custom"></a><dl>
<dt><b>GUID_TFCAT_PROPSTYLE_CUSTOM</b></dt>
</dl>
</td>
<td width="60%">
The property is a custom property.

</td>
</tr>
</table>

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pguid</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory
      </a>



<a href="/windows/desktop/api/msctf/nn-msctf-itfreadonlyproperty">ITfReadOnlyProperty</a>



<a href="/windows/desktop/TSF/properties">Properties</a>