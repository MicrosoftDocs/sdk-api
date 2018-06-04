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

# PSGetNameFromPropertyKey function


## -description


Retrieves the canonical name of the property, given its <a href="shell.PROPERTYKEY">PROPERTYKEY</a>.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure that identifies the requested property.


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
Indicates that the <a href="shell.PROPERTYKEY">PROPERTYKEY</a> does not exist in the schema subsystem cache.

</td>
</tr>
</table>
 




## -remarks



Retrieves a canonical name for a specified property key. Like property keys, canonical names uniquely identify a property. For example, <code>System.Keywords</code> is the canonical name for <code>PKEY_Keywords</code>. This function succeeds only for properties registered as part of the property schema.

It is the responsibility of the calling application to use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the string referred to by <i>ppszCanonicalName</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSGetNameFromPropertyKey">PSGetNameFromPropertyKey</a> to read a value from serialized property storage.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PWSTR pszName;

HRESULT hr = PSGetNameFromPropertyKey(PKEY_Keywords, &amp;pszName);

if (SUCCEEDED(hr))
{
    // pszName now contains L"System.Keywords"
 
    CoTaskMemFree(pszName);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.IPropertyDescription_GetCanonicalName">IPropertyDescription::GetCanonicalName</a>



<a href="shell.PSGetPropertyDescriptionByName">PSGetPropertyDescriptionByName</a>



<a href="shell.PSGetPropertyKeyFromName">PSGetPropertyKeyFromName</a>



<a href="shell.PSStringFromPropertyKey">PSStringFromPropertyKey</a>
 

 

