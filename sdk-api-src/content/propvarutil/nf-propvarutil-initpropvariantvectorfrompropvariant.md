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

# InitPropVariantVectorFromPropVariant function


## -description


Initializes a vector element in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure with a value stored in another <b>PROPVARIANT</b>.


## -parameters




### -param propvarSingle [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains a single value.


### -param ppropvarVector [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is used to convert a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains a single value into a vector value.

For simple source types, this function initializes the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> as a vector of one element.

For a source that contains a string, this function initializes the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> with zero or more substrings taken from the source string, treating semicolons as delimiters. See <a href="shell.InitPropVariantFromStringAsVector">InitPropVariantFromStringAsVector</a> for more details.

The following input types are supported:
            
                

<ul>
<li>VT_I2</li>
<li>VT_UI2</li>
<li>VT_I4</li>
<li>VT_UI4</li>
<li>VT_I8</li>
<li>VT_UI8</li>
<li>VT_R8</li>
<li>VT_BOOL</li>
<li>VT_DATE</li>
<li>VT_FILETIME</li>
<li>VT_BSTR</li>
<li>VT_LPWSTR</li>
</ul>
Additional types may be supported in the future.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantVectorFromPropVariant">InitPropVariantVectorFromPropVariant</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvarSource;
// Assume propvarSource is initialized and valid.

if (PropVariantGetElementCount(propvarSource) == 1)
{
    PROPVARIANT propvar;

    HRESULT hr = InitPropVariantVectorFromPropVariant(propvarSource, &amp;propvar);

    if (SUCCEEDED(hr))
    {
       // propvar now is valid and is either VT_EMPTY or contains a vector.
       PropVariantClear(&amp;propvar);
    }</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromStringAsVector">InitPropVariantFromStringAsVector</a>



<a href="shell.PropVariantGetElem">PropVariantGetElem</a>



<a href="shell.PropVariantGetElementCount">PropVariantGetElementCount</a>
 

 

