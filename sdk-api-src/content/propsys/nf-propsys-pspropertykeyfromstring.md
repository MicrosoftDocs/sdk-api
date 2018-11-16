---
UID: NF:propsys.PSPropertyKeyFromString
title: PSPropertyKeyFromString function
author: windows-sdk-content
description: Converts a string to a PROPERTYKEY structure.
old-location: properties\PSPropertyKeyFromString.htm
tech.root: properties
ms.assetid: 9096912a-14ad-4a45-a564-08f98fce3f96
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PSPropertyKeyFromString, PSPropertyKeyFromString function [Windows Properties], _shell_PSPropertyKeyFromString, properties.PSPropertyKeyFromString, propsys/PSPropertyKeyFromString, shell.PSPropertyKeyFromString
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
 - PSPropertyKeyFromString
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- PSPropertyKeyFromString
: 
---

# PSPropertyKeyFromString function


## -description


Converts a string to a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> structure.


## -parameters




### -param pszString [in]

Type: <b>LPCWSTR</b>

Pointer to a null-terminated, Unicode string to be converted.


### -param pkey [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a>*</b>

When this function returns, contains a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string to be converted must be formatted as <code>"{fmtid} pid"</code>. For instance, the string that corresponds to <code>PKEY_Title</code> is: <code>"{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 2"</code>. <a href="https://msdn.microsoft.com/en-us/library/Bb762089(v=VS.85).aspx">PSStringFromPropertyKey</a> outputs strings in this format.

This function succeeds for any valid property key string, even if the property does not exist in the property schema.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762085(v=VS.85).aspx">PSPropertyKeyFromString</a>.

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




<a href="https://msdn.microsoft.com/en-us/library/Bb762081(v=VS.85).aspx">PSGetPropertyKeyFromName</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762089(v=VS.85).aspx">PSStringFromPropertyKey</a>
 

 

