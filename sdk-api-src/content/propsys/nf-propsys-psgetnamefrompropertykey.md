---
UID: NF:propsys.PSGetNameFromPropertyKey
title: PSGetNameFromPropertyKey function (propsys.h)
description: Retrieves the canonical name of the property, given its PROPERTYKEY.
old-location: properties\PSGetNameFromPropertyKey.htm
tech.root: properties
ms.assetid: 7ab6b5e8-8202-4553-ba9b-be7cf9f9381d
ms.date: 12/05/2018
ms.keywords: PSGetNameFromPropertyKey, PSGetNameFromPropertyKey function [Windows Properties], properties.PSGetNameFromPropertyKey, propsys/PSGetNameFromPropertyKey, shell.PSGetNameFromPropertyKey, shell_PSGetNameFromPropertyKey
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PSGetNameFromPropertyKey
 - propsys/PSGetNameFromPropertyKey
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetNameFromPropertyKey
---

# PSGetNameFromPropertyKey function


## -description

Retrieves the canonical name of the property, given its <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>.

## -parameters

### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> structure that identifies the requested property.

### -param ppszCanonicalName [out]

Type: <b>PWSTR*</b>

When this function returns, contains a pointer to the property name as a null-terminated Unicode string.

## -returns

Type: <b>HRESULT</b>

Returns one of the following values.

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
The property's canonical name is obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a> does not exist in the schema subsystem cache.

</td>
</tr>
</table>

## -remarks

Retrieves a canonical name for a specified property key. Like property keys, canonical names uniquely identify a property. For example, <code>System.Keywords</code> is the canonical name for <code>PKEY_Keywords</code>. This function succeeds only for properties registered as part of the property schema.

It is the responsibility of the calling application to use <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a> to release the string referred to by <i>ppszCanonicalName</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetnamefrompropertykey">PSGetNameFromPropertyKey</a> to read a value from serialized property storage.


```cpp
PWSTR pszName;

HRESULT hr = PSGetNameFromPropertyKey(PKEY_Keywords, &pszName);

if (SUCCEEDED(hr))
{
    // pszName now contains L"System.Keywords"
 
    CoTaskMemFree(pszName);
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-getcanonicalname">IPropertyDescription::GetCanonicalName</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionbyname">PSGetPropertyDescriptionByName</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertykeyfromname">PSGetPropertyKeyFromName</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psstringfrompropertykey">PSStringFromPropertyKey</a>