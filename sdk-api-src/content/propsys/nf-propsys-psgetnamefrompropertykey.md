---
UID: NF:propsys.PSGetNameFromPropertyKey
title: PSGetNameFromPropertyKey function
author: windows-sdk-content
description: Retrieves the canonical name of the property, given its PROPERTYKEY.
old-location: properties\PSGetNameFromPropertyKey.htm
tech.root: properties
ms.assetid: 7ab6b5e8-8202-4553-ba9b-be7cf9f9381d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PSGetNameFromPropertyKey, PSGetNameFromPropertyKey function [Windows Properties], properties.PSGetNameFromPropertyKey, propsys/PSGetNameFromPropertyKey, shell.PSGetNameFromPropertyKey, shell_PSGetNameFromPropertyKey
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSGetNameFromPropertyKey
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- PSGetNameFromPropertyKey
: 
---

# PSGetNameFromPropertyKey function


## -description


Retrieves the canonical name of the property, given its <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a>.


## -parameters




### -param propkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> structure that identifies the requested property.


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
Indicates that the <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> does not exist in the schema subsystem cache.

</td>
</tr>
</table>
 




## -remarks



Retrieves a canonical name for a specified property key. Like property keys, canonical names uniquely identify a property. For example, <code>System.Keywords</code> is the canonical name for <code>PKEY_Keywords</code>. This function succeeds only for properties registered as part of the property schema.

It is the responsibility of the calling application to use <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the string referred to by <i>ppszCanonicalName</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776502(v=VS.85).aspx">PSGetNameFromPropertyKey</a> to read a value from serialized property storage.

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




<a href="https://msdn.microsoft.com/library/Bb761525(v=VS.85).aspx">IPropertyDescription::GetCanonicalName</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776504(v=VS.85).aspx">PSGetPropertyDescriptionByName</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762081(v=VS.85).aspx">PSGetPropertyKeyFromName</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762089(v=VS.85).aspx">PSStringFromPropertyKey</a>
 

 

