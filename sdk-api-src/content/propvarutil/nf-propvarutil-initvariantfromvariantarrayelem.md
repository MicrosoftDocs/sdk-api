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

# InitVariantFromVariantArrayElem function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure with a value stored in another <b>VARIANT</b> structure.


## -parameters




### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param iElem [in]

Type: <b>ULONG</b>

Index of one of the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure elements.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function works for <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structures of the following types:
                
                

<ul>
<li>VT_BSTR</li>
<li>VT_BOOL</li>
<li>VT_I2</li>
<li>VT_I4</li>
<li>VT_I8</li>
<li>VT_U12</li>
<li>VT_U14</li>
<li>VT_U18</li>
<li>VT_DATE</li>
<li>VT_ARRAY | (any one of VT_BSTR, VT_BOOL, VT_I2, VT_I4, VT_I8, VT_U12, VT_U14, VT_U18, VT_DATE)</li>
</ul>
Additional types may be supported in the future.

This function extracts a single value from the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure and uses that value to initialize the output <b>VARIANT</b> structure. The calling application must use <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a> to free the <b>VARIANT</b> referred to by <i>pvar</i> when it is no longer needed.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is an array, <i>iElem</i> must be less than the number of elements in the array.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> has a single value, <i>iElem</i> must be 0.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is empty, this function always returns an error code.

You can use <a href="shell.VariantGetElementCount">VariantGetElementCount</a> to obtain the number of elements in the array or array.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromVariantArrayElem">InitVariantFromVariantArrayElem</a> in an iteration statement to access the values in a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume var is initialized and valid.
UINT cElem = VariantGetElementCount(var);
HRESULT hr = &lt;mark type="const"&gt;S_OK&lt;/mark&gt;;

for (UINT iElem = 0; SUCCEEDED(hr) &amp;&amp; iElem &lt; cElem; iElem ++)
{
    VARIANT varElem = {0};

    hr = InitVariantFromVariantArrayElem(var, iElem, &amp;varElem);

    if (SUCCEEDED(hr))
    {
        // varElem is now valid.
        VariantClear(&amp;varElem);
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromPropVariantVectorElem">InitPropVariantFromPropVariantVectorElem</a>



<a href="shell.VariantGetElem">VariantGetElem</a>
 

 

