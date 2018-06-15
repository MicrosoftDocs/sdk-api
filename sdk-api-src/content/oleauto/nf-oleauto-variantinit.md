---
UID: NF:oleauto.VariantInit
title: VariantInit function
author: windows-sdk-content
description: Initializes a variant.
old-location: automat\variantinit.htm
old-project: automat
ms.assetid: 96aeb671-5528-4d3c-8e70-313716550b42
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: VariantInit, VariantInit function [Automation], _oa96_VariantInit, automat.variantinit, oleauto/VariantInit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VariantInit
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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



The <b>VariantInit</b> function initializes the VARIANTARG by setting the <b>vt</b> field to VT_EMPTY. Unlike <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear.md">VariantClear</a>, this function does not interpret the current contents of the VARIANTARG. Use <b>VariantInit</b> to initialize new local variables of type VARIANTARG (or VARIANT).


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
 

 

