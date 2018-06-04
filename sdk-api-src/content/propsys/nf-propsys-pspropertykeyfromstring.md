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

# PSPropertyKeyFromString function


## -description


Converts a string to a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure.


## -parameters




### -param pszString [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated, Unicode string to be converted.


### -param pkey [out]

Type: <b><a href="shell.PROPERTYKEY">PROPERTYKEY</a>*</b>

When this function returns, contains a pointer to a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string to be converted must be formatted as <code>"{fmtid} pid"</code>. For instance, the string that corresponds to <code>PKEY_Title</code> is: <code>"{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 2"</code>. <a href="shell.PSStringFromPropertyKey">PSStringFromPropertyKey</a> outputs strings in this format.

This function succeeds for any valid property key string, even if the property does not exist in the property schema.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PSPropertyKeyFromString">PSPropertyKeyFromString</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>PROPERTYKEY key;

HRESULT hr = PSPropertyKeyFromString(L"{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 2", &amp;key);

if (SUCCEEDED(hr))
{
    // The key variable is now valid.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSGetPropertyKeyFromName">PSGetPropertyKeyFromName</a>



<a href="shell.PSStringFromPropertyKey">PSStringFromPropertyKey</a>
 

 

