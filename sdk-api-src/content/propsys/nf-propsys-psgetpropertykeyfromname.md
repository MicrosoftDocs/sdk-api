---
UID: NF:propsys.PSGetPropertyKeyFromName
title: PSGetPropertyKeyFromName function (propsys.h)
description: Gets the property key for a canonical property name.
old-location: properties\PSGetPropertyKeyFromName.htm
tech.root: properties
ms.assetid: a80301d9-8b4e-4a17-8e24-4362ba3b1ab5
ms.date: 12/05/2018
ms.keywords: PSGetPropertyKeyFromName, PSGetPropertyKeyFromName function [Windows Properties], properties.PSGetPropertyKeyFromName, propsys/PSGetPropertyKeyFromName, shell.PSGetPropertyKeyFromName, shell_PSGetPropertyKeyFromName
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
 - PSGetPropertyKeyFromName
 - propsys/PSGetPropertyKeyFromName
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
 - PSGetPropertyKeyFromName
---

# PSGetPropertyKeyFromName function


## -description

Gets the property key for a canonical property name.

## -parameters

### -param pszName [in]

Type: <b>PCWSTR</b>

Pointer to a property name as a null-terminated, Unicode string.

### -param ppropkey [out]

Type: <b><a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey">PROPERTYKEY</a>*</b>

When this function returns, contains the requested property key.

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
Property key structure was obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pszName</i> parameter is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_ELEMENTNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The canonical property name does not exist in the schema subsystem cache.

</td>
</tr>
</table>

## -remarks

Property keys uniquely identify a property. For example, <code>PKEY_Keywords</code> corresponds to <code>System.Keywords</code>. This function succeeds only for properties registered as part of the property schema.

See <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescriptionbyname">PSGetPropertyDescriptionByName</a> for a list of legacy property names that are also supported by the function.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertykeyfromname">PSGetPropertyKeyFromName</a> to obtain the property key for <code>System.Keywords</code>.


```cpp
PROPERTYKEY key;

HRESULT hr = PSGetPropertyKeyFromName(L"System.Keywords", &key);

if (SUCCEEDED(hr))
{
    // The property key is now valid.
}
```

## -see-also

<a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-getpropertykey">IPropertyDescription::GetPropertyKey</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psgetnamefrompropertykey">PSGetNameFromPropertyKey</a>



<a href="/windows/desktop/api/propsys/nf-propsys-psgetpropertydescription">PSGetPropertyDescription</a>



<a href="/windows/desktop/api/propsys/nf-propsys-pspropertykeyfromstring">PSPropertyKeyFromString</a>