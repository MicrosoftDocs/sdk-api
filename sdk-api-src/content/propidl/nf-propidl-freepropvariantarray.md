---
UID: NF:propidl.FreePropVariantArray
title: FreePropVariantArray function
author: windows-sdk-content
description: Frees the memory and references used by an array of PROPVARIANT structures.
old-location: properties\FreePropVariantArray.htm
old-project: properties
ms.assetid: 5033557c-d43c-42b1-ae4e-0fb0569d697a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: FreePropVariantArray, FreePropVariantArray function [Windows Properties], _shell_FreePropVariantArray, properties.FreePropVariantArray, propidl/FreePropVariantArray, shell.FreePropVariantArray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PROFILEINFOW, *LPPROFILEINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - FreePropVariantArray
product: Windows
targetos: Windows
req.lib: Ole32.lib
req.dll: Ole32.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# FreePropVariantArray function


## -description


Frees the memory and references used by an array of <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures.


## -parameters




### -param cVariants [in]

Type: <b>ULONG</b>

The number of elements in the array specified by <i>rgvars</i>.


### -param rgvars [in, out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

Array of <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structures to free. When this function successfully returns, the <b>PROPVARIANT</b> structures in the array are zeroed and their type is set to VT_EMPTY.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function releases the memory and references held by each structure in the array before setting the structures to zero.

This function performs the same action as <a href="https://www.bing.com/search?q=ClearPropVariantArray">ClearPropVariantArray</a>, but returns an <b>HRESULT</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://www.bing.com/search?q=FreePropVariantArray">FreePropVariantArray</a>


<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT rgpropvar[5];
// Assume all 5 propvariants are initialized and valid.

FreePropVariantArray(ARRAYSIZE(rgpropvar), rgpropvar);</pre>
</td>
</tr>
</table></span></div>


