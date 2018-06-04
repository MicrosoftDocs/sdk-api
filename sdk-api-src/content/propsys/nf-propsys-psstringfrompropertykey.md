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

# PSStringFromPropertyKey function


## -description


Creates a string that identifies a property from that property's key.


## -parameters




### -param pkey [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="shell.PROPERTYKEY">PROPERTYKEY</a> structure that identifies a property.


### -param psz [out]

Type: <b>LPWSTR</b>

Pointer to a buffer that receives the output string. The buffer should be large enough to contain PKEYSTR_MAX <b>WCHAR</b><b>s</b>.


### -param cch [in]

Type: <b>UINT</b>

The length of the buffer pointed to by <i>psz</i>, in <b>WCHAR</b><b>s</b>.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string format retrieved is <code>"{propkey.fmtid} propkey.pid"</code>. For example, the output string for <code>PKEY_Title</code> is <code>"{F29F85E0-4FF9-1068-AB91-08002B27B3D9} 2"</code>.


#### Examples

The following example, to be included as part of a larger program, demonstrates the use of <a href="shell.PSPropertyKeyFromString">PSPropertyKeyFromString</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>WCHAR szKey[PKEYSTR_MAX]

HRESULT hr = PSStringFromPropertyKey(PKEY_Title, szKey, ARRAYSIZE(szKey));

if (SUCCEEDED(hr))
{
    // szKey is now valid.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PSGetNameFromPropertyKey">PSGetNameFromPropertyKey</a>



<a href="shell.PSPropertyKeyFromString">PSPropertyKeyFromString</a>
 

 

