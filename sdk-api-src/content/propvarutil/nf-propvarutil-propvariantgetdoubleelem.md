---
UID: NF:propvarutil.PropVariantGetDoubleElem
title: PropVariantGetDoubleElem function
author: windows-sdk-content
description: Extracts a single double element from a PROPVARIANT structure of type VT_R8, VT_VECTOR | VT_R8, or VT_ARRAY | VT_R8.
old-location: properties\PropVariantGetDoubleElem.htm
tech.root: properties
ms.assetid: 387e23df-bfbd-42c0-adef-dc53ba95a9f2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropVariantGetDoubleElem, PropVariantGetDoubleElem function [Windows Properties], _shell_PropVariantGetDoubleElem, properties.PropVariantGetDoubleElem, propvarutil/PropVariantGetDoubleElem, shell.PropVariantGetDoubleElem
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PropVariantGetDoubleElem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantGetDoubleElem function


## -description


Extracts a single <b>double</b> element from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure of type <code>VT_R8</code>, <code>VT_VECTOR | VT_R8</code>, or <code>VT_ARRAY | VT_R8</code>.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param iElem [in]

Type: <b>ULONG</b>

Specifies vector or array index; otherwise, <i>iElem</i> must be 0.


### -param pnVal [out]

Type: <b>DOUBLE*</b>

When this function returns, contains the extracted double value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <code>VT_R8</code>, <i>iElem</i> must be 0. Otherwise <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="https://msdn.microsoft.com/en-us/library/Bb776522(v=VS.85).aspx">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.

The following example uses this function to loop through the values in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// assume propvar is initialized and valid

if ((propvar.vt &amp; VT_TYPEMASK) == VT_R8)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = &lt;mark type="const"&gt;S_OK&lt;/mark&gt;;
    
    for (UINT iElem = 0; SUCCEEDED(hr) &amp;&amp; iElem &lt; cElem; iElem ++)
    {
        DOUBLE nValue;
        hr = PropVariantGetDoubleElem(propvar, iElem, &amp;nValue);
    
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




<a href="https://msdn.microsoft.com/en-us/library/Bb776521(v=VS.85).aspx">PropVariantGetElem</a>
 

 

