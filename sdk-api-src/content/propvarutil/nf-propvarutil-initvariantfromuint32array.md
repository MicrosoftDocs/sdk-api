---
UID: NF:propvarutil.InitVariantFromUInt32Array
title: InitVariantFromUInt32Array function
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of unsigned 32-bit integer values.
old-location: properties\InitVariantFromUInt32Array.htm
old-project: properties
ms.assetid: b08e61bc-8b76-4baf-acf7-9eb97e521b65
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: InitVariantFromUInt32Array, InitVariantFromUInt32Array function [Windows Properties], _shell_InitVariantFromUInt32Array, properties.InitVariantFromUInt32Array, propvarutil/InitVariantFromUInt32Array, shell.InitVariantFromUInt32Array
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	InitVariantFromUInt32Array
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# InitVariantFromUInt32Array function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure with an array of unsigned 32-bit integer values.


## -parameters




### -param prgn [in]

Type: <b>const ULONG*</b>

Pointer to the source array of <b>ULONG</b> values.


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



Creates a VT_ARRAY | VT_UI4 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromUInt32Array">InitVariantFromUInt32Array</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ULONG rgLongs[] = {4, 2};
VARIANT var;

HRESULT hr = InitVariantFromUInt32Array(rgLongs, ARRAYSIZE(rgLongs), &amp;var);

if (SUCCEEDED(hr))                            
{
    // var now is valid and has type VT_ARRAY | VT_UI4.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromUInt32Vector">InitPropVariantFromUInt32Vector</a>



<a href="shell.InitVariantFromUInt32">InitVariantFromUInt32</a>



<a href="shell.VariantToUInt32Array">VariantToUInt32Array</a>
 

 

