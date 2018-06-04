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

# ClearVariantArray function


## -description


Frees the memory and references used by an array of <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structures stored in an array.


## -parameters




### -param pvars [in]

Type: <b>VARIANT*</b>

Array of <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structures to free.


### -param cvars

TBD




#### - cVars [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>pvars</i>.


## -returns



No return value.




## -remarks



This function releases the memory and references held by each structure in the array before it sets the structures to zero.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.ClearVariantArray">ClearVariantArray</a>


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT rgpropvar[5];
// Assume all 5 variants are initialized and valid.

ClearVariantArray(rgpropvar, ARRAYSIZE(rgpropvar));</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.ClearPropVariantArray">ClearPropVariantArray</a>



<a href="shell.FreePropVariantArray">FreePropVariantArray</a>
 

 

