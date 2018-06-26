---
UID: NF:propvarutil.PropVariantGetUInt64Elem
title: PropVariantGetUInt64Elem function
author: windows-sdk-content
description: Extracts a single unsigned Int64 element from a PROPVARIANT structure of type VT_UI8, VT_VECTOR | VT_UI8, or VT_ARRAY | VT_UI8.
old-location: properties\PropVariantGetUInt64Elem.htm
old-project: properties
ms.assetid: 35955104-b567-4c4f-850a-0a4778673ce8
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantGetUInt64Elem, PropVariantGetUInt64Elem function [Windows Properties], _shell_PropVariantGetUInt64Elem, properties.PropVariantGetUInt64Elem, propvarutil/PropVariantGetUInt64Elem, shell.PropVariantGetUInt64Elem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantGetUInt64Elem
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PropVariantGetUInt64Elem function


## -description


Extracts a single unsigned Int64 element from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure of type VT_UI8, VT_VECTOR | VT_UI8, or VT_ARRAY | VT_UI8.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param iElem [in]

Type: <b>ULONG</b>

The vector or array index; otherwise, <i>iElem</i> must be 0.


### -param pnVal [out]

Type: <b>ULONGLONG*</b>

When this function returns, contains the extracted Int64 value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function works for <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures of the following types: 

                

<ul>
<li>VT_UI8</li>
<li>VT_VECTOR | VT_UI8</li>
<li>VT_ARRAY | VT_UI8</li>
</ul>
If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_UI8, <i>iElem</i> must be 0. Otherwise <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="shell.PropVariantGetElementCount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantGetUInt64Elem">PropVariantGetUInt64Elem</a> with an iteration statement to access the values in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid

if ((propvar.vt &amp; VT_TYPEMASK) == VT_UI8)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = &lt;mark type="const"&gt;S_OK&lt;/mark&gt;;

    for (UINT iElem = 0; SUCCEEDED(hr) &amp;&amp; iElem &lt; cElem; iElem ++)
    {
        ULONGLONG nValue;
        hr = PropVariantGetUInt64Elem(propvar, iElem, &amp;nValue);

        if (SUCCEEDED(hr))
        {
            // nValue is valid now
        }
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.PropVariantGetElem">PropVariantGetElem</a>
 

 

