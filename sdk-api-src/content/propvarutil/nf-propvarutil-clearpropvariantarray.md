---
UID: NF:propvarutil.ClearPropVariantArray
title: ClearPropVariantArray function
author: windows-driver-content
description: Frees the memory and references used by an array of PROPVARIANT structures stored in an array.
old-location: properties\ClearPropVariantArray.htm
old-project: properties
ms.assetid: e8d7f951-8a9e-441b-9fa7-bf21cf08c8ac
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: ClearPropVariantArray, ClearPropVariantArray function [Windows Properties], _shell_ClearPropVariantArray, properties.ClearPropVariantArray, propvarutil/ClearPropVariantArray, shell.ClearPropVariantArray
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	ClearPropVariantArray
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ClearPropVariantArray function


## -description


Frees the memory and references used by an array of <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures stored in an array.


## -parameters




### -param rgPropVar [in]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Array of <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures to free.


### -param cVars [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>rgPropVar</i>.


## -returns



No return value.




## -remarks



This function releases the memory and references held by each structure in the array before setting the structures to zero.

This function performs the same action as <a href="shell.FreePropVariantArray">FreePropVariantArray</a>, but <b>FreePropVariantArray</b> returns an <b>HRESULT</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.ClearPropVariantArray">ClearPropVariantArray</a>


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT rgpropvar[5];
// Assume all 5 propvariants are initialized and valid.

ClearPropVariantArray(rgpropvar, ARRAYSIZE(rgpropvar));</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.ClearVariantArray">ClearVariantArray</a>
 

 

