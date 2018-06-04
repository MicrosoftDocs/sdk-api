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

# VariantInit function


## -description


Initializes a variant.


## -parameters




### -param pvarg [out]

The variant to initialize.


## -returns



This function does not return a value.




## -remarks



The <b>VariantInit</b> function initializes the VARIANTARG by setting the <b>vt</b> field to VT_EMPTY. Unlike <a href="28741D81-8404-4F85-95D3-5C209EC13835">VariantClear</a>, this function does not interpret the current contents of the VARIANTARG. Use <b>VariantInit</b> to initialize new local variables of type VARIANTARG (or VARIANT).


#### Examples

The following example shows how to initialize an array of variants, where <code>celt</code> is the number of elements in the array.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>for(int i = 0; i &gt; celt; ++i)
   VariantInit(&amp;rgvar[i]);</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f0940eea-077f-4b68-9dac-d49e3fc62e43">Variant Manipulation Functions</a>
 

 

