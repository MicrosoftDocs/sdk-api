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

# VariantToBooleanArrayAlloc function


## -description


Allocates an array of <b>BOOL</b> values then extracts data from a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure into that array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param pprgf [out]

Type: <b>BOOL**</b>

When this function returns, contains a pointer to an array of <b>BOOL</b> values extracted from the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains a pointer to the count of elements extracted from the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> to hold an array of <b>BOOL</b> values.

If the source <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> is of type VT_ARRAY | VT_BOOL, this function extracts an array of <b>BOOL</b> values into a newly allocated array. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the array pointed to by <i>pprgf</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToBooleanArrayAlloc">VariantToBooleanArrayAlloc</a> to access an array of <b>BOOL</b> values stored in a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume variable var is initialized and valid. 
// The application expects var to contain an array of BOOL values.
BOOL *prgFlags;
ULONG cElems;

HRESULT hr = VariantToBooleanArrayAlloc(var, &amp;prgFlags, &amp;cElems);

if (SUCCEEDED(hr))
{
     // prgFlags now points to a vector of cElems BOOLs.
     CoTaskMemFree(prgFlags);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromBooleanArray">InitVariantFromBooleanArray</a>



<a href="shell.PropVariantToBooleanVector">PropVariantToBooleanVector</a>



<a href="shell.VariantToBooleanArray">VariantToBooleanArray</a>
 

 

