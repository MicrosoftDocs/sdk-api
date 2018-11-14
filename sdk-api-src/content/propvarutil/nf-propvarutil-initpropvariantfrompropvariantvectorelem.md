---
UID: NF:propvarutil.InitPropVariantFromPropVariantVectorElem
title: InitPropVariantFromPropVariantVectorElem function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a specified PROPVARIANT vector element.
old-location: properties\InitPropVariantFromPropVariantVectorElem.htm
tech.root: properties
ms.assetid: 4618e63a-8afa-45d4-b0b0-cd1dae064ba4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitPropVariantFromPropVariantVectorElem, InitPropVariantFromPropVariantVectorElem function [Windows Properties], properties.InitPropVariantFromPropVariantVectorElem, propvarutil/InitPropVariantFromPropVariantVectorElem, shell.InitPropVariantFromPropVariantVectorElem, shell_InitPropVariantFromPropVariantVectorElem
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
 - InitPropVariantFromPropVariantVectorElem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitPropVariantFromPropVariantVectorElem
: 
---

# InitPropVariantFromPropVariantVectorElem function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a specified <b>PROPVARIANT</b> vector element.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param iElem [in]

Type: <b>ULONG</b>

The index of the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure element.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function works for <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures of the following types:

                

<ul>
<li>VT_LPWSTR</li>
<li>VT_BSTR</li>
<li>VT_BOOL</li>
<li>VT_I2</li>
<li>VT_I4</li>
<li>VT_I8</li>
<li>VT_U12</li>
<li>VT_U14</li>
<li>VT_U18</li>
<li>VT_FILETIME</li>
<li>VT_VECTOR | (any one of VT_LPWSTR, VT_BSTR, VT_BOOL, VT_I2, VT_I4, VT_I8, VT_U12, VT_U14, VT_U18, VT_FILETIME)</li>
<li>VT_ARRAY | (any one of VT_BSTR, VT_BOOL, VT_I2, VT_I4, VT_I8, VT_U12, VT_U14, VT_U18)</li>
</ul>
Additional types may be supported in the future.

This function extracts a single value from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure and uses that value to initialize the output <b>PROPVARIANT</b> structure. The calling application must use <a href="https://msdn.microsoft.com/en-us/library/ms712573(v=VS.85).aspx">PropVariantClear</a> to free the <b>PROPVARIANT</b> referred to by <i>ppropvar</i> when it is no longer needed.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> is a vector or array, <i>iElem</i> must be less than the number of elements in the vector or array.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has a single value, <i>iElem</i> must be 0.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> is empty, this function always returns an error code.

You can use <a href="https://msdn.microsoft.com/en-us/library/Bb776522(v=VS.85).aspx">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.


#### Examples

The following code example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762303(v=VS.85).aspx">InitPropVariantFromPropVariantVectorElem</a> in an iteration statement to access the values in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume propvar is initialized and valid.
UINT cElem = PropVariantGetElementCount(propvar);
HRESULT hr = &lt;mark type="const"&gt;S_OK&lt;/mark&gt;;

for (UINT iElem = 0; SUCCEEDED(hr) &amp;&amp; iElem &lt; cElem; iElem ++)
{
    PROPVARIANT propvarElem = {0};

    hr = InitPropVariantFromPropVariantVectorElem(propvar, iElem, &amp;propvarElem);

    if (SUCCEEDED(hr))
    {
        // propvarElem is now valid.

        PropVariantClear(&amp;propvarElem);
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb776521(v=VS.85).aspx">PropVariantGetElem</a>
 

 

