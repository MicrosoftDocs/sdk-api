---
UID: NF:propvarutil.ClearVariantArray
title: ClearVariantArray function
author: windows-sdk-content
description: Frees the memory and references used by an array of VARIANT structures stored in an array.
old-location: properties\ClearVariantArray.htm
tech.root: properties
ms.assetid: 8126392e-d86c-420c-9f0d-ca7cb97030b0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ClearVariantArray, ClearVariantArray function [Windows Properties], _shell_ClearVariantArray, properties.ClearVariantArray, propvarutil/ClearVariantArray, shell.ClearVariantArray
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
 - ClearVariantArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# ClearVariantArray function


## -description


Frees the memory and references used by an array of <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structures stored in an array.


## -parameters




### -param pvars [in]

Type: <b>VARIANT*</b>

Array of <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structures to free.


### -param cvars [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>pvars</i>.


## -returns



No return value.




## -remarks



This function releases the memory and references held by each structure in the array before it sets the structures to zero.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762284(v=VS.85).aspx">ClearVariantArray</a>


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




<a href="https://msdn.microsoft.com/en-us/library/Bb762283(v=VS.85).aspx">ClearPropVariantArray</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762285(v=VS.85).aspx">FreePropVariantArray</a>
 

 

