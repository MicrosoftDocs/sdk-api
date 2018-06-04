---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# PSGetPropertyKeyFromName function


## -description


Gets the property key for a canonical property name.


## -parameters




### -param pszName [in]

Type: <b>PCWSTR</b>

Pointer to a property name as a null-terminated, Unicode string.


### -param ppropkey [out]

Type: <b><a href="shell.PROPERTYKEY">PROPERTYKEY</a>*</b>

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

See <a href="shell.PSGetPropertyDescriptionByName">PSGetPropertyDescriptionByName</a> for a list of legacy property names that are also supported by the function.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetPropertyKeyFromName">PSGetPropertyKeyFromName</a> to obtain the property key for <code>System.Keywords</code>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPERTYKEY key;

HRESULT hr = PSGetPropertyKeyFromName(L"System.Keywords", &amp;key);

if (SUCCEEDED(hr))
{
    // The property key is now valid.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.IPropertyDescription_GetPropertyKey">IPropertyDescription::GetPropertyKey</a>



<a href="shell.PSGetNameFromPropertyKey">PSGetNameFromPropertyKey</a>



<a href="shell.PSGetPropertyDescription">PSGetPropertyDescription</a>



<a href="shell.PSPropertyKeyFromString">PSPropertyKeyFromString</a>
 

 

