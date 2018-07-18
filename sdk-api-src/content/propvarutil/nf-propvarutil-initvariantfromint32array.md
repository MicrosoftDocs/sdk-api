---
UID: NF:propvarutil.InitVariantFromInt32Array
title: InitVariantFromInt32Array function
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of 32-bit integer values.
old-location: properties\InitVariantFromInt32Array.htm
old-project: properties
ms.assetid: 0805d510-ee9c-4f10-978d-c34d572488f9
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: InitVariantFromInt32Array, InitVariantFromInt32Array function [Windows Properties], _shell_InitVariantFromInt32Array, properties.InitVariantFromInt32Array, propvarutil/InitVariantFromInt32Array, shell.InitVariantFromInt32Array
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - InitVariantFromInt32Array
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitVariantFromInt32Array function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure with an array of 32-bit integer values.


## -parameters




### -param prgn [in]

Type: <b>const LONG*</b>

Pointer to the source array of <b>LONG</b> values.


### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgn</i>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_ARRAY | VT_I4 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromInt32Array">InitVariantFromInt32Array</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LONG rgLongs[] = {4, 2};
VARIANT var;

HRESULT hr = InitVariantFromInt32Array(rgLongs, ARRAYSIZE(rgLongs), &amp;var);

if (SUCCEEDED(hr))                            
{
    // var now is valid and has type VT_ARRAY | VT_I4.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromInt32Vector">InitPropVariantFromInt32Vector</a>



<a href="shell.InitVariantFromInt32">InitVariantFromInt32</a>



<a href="shell.VariantToInt32Array">VariantToInt32Array</a>
 

 

