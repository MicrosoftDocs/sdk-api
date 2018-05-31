---
UID: NF:propvarutil.PropVariantGetInt32Elem
title: PropVariantGetInt32Elem function
author: windows-sdk-content
description: Extracts a single Int32 element from a PROPVARIANT of type VT_I4, VT_VECTOR | VT_I4, or VT_ARRAY | VT_I4.
old-location: properties\PropVariantGetInt32Elem.htm
old-project: properties
ms.assetid: de7dc6d4-d85a-44cb-8af7-840fd6e68d5c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantGetInt32Elem, PropVariantGetInt32Elem function [Windows Properties], _shell_PropVariantGetInt32Elem, properties.PropVariantGetInt32Elem, propvarutil/PropVariantGetInt32Elem, shell.PropVariantGetInt32Elem
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PropVariantGetInt32Elem
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropVariantGetInt32Elem function


## -description


Extracts a single Int32 element from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> of type VT_I4, VT_VECTOR | VT_I4, or VT_ARRAY | VT_I4.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param iElem [in]

Type: <b>ULONG</b>

The vector or array index; otherwise, <i>iElem</i> must be 0.


### -param pnVal [out]

Type: <b>LONG*</b>

When this function, contains the extracted Int32 value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function works for <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures of the following types: 
          
                

<ul>
<li>VT_I4</li>
<li>VT_VECTTOR | VT_I4</li>
<li>VT_ARRAY | VT_I4</li>
</ul>
If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_I4, iElem must be 0. Otherwise, <i>iElem</i>  must be less than the number of elements in the vector or array. You can use <a href="shell.PropVariantGetElementCount">PropVariantGetElementCount</a>  to obtain the number of elements in the vector or array.


#### Examples

The following example uses this <a href="shell.PropVariantGetInt32Elem">PropVariantGetInt32Elem</a> with an interation statement to access the values in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// assume propvar is initialized and valid

if ((propvar.vt &amp; VT_TYPEMASK) == VT_I4)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = &lt;mark type="const"&gt;S_OK&lt;/mark&gt;;

    for (UINT iElem = 0; SUCCEEDED(hr) &amp;&amp; iElem &lt; cElem; iElem ++)
    {
        LONG nValue;
        hr = PropVariantGetInt32Elem(propvar, iElem, &amp;nValue);

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
 

 

