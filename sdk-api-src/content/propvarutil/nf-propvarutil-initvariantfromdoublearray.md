---
UID: NF:propvarutil.InitVariantFromDoubleArray
title: InitVariantFromDoubleArray function
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of values of type DOUBLE.
old-location: properties\InitVariantFromDoubleArray.htm
tech.root: properties
ms.assetid: 781b6999-4551-499d-ba37-0a7e05fc6eab
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: InitVariantFromDoubleArray, InitVariantFromDoubleArray function [Windows Properties], _shell_InitVariantFromDoubleArray, properties.InitVariantFromDoubleArray, propvarutil/InitVariantFromDoubleArray, shell.InitVariantFromDoubleArray
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
 - InitVariantFromDoubleArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitVariantFromDoubleArray function


## -description


Initializes a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure with an array of values of type DOUBLE.


## -parameters




### -param prgn [in]

Type: <b>const DOUBLE*</b>

Pointer to the source array of DOUBLE values.


### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgn</i>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_ARRAY | VT_R8 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitVariantFromDoubleArray">InitVariantFromDoubleArray</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>DOUBLE rgDoubles[] = {34.7, 12.0};
VARIANT var;

HRESULT hr = InitVariantFromDoubleArray(rgDoubles, ARRAYSIZE(rgDoubles), &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_R8.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromDoubleVector">InitPropVariantFromDoubleVector</a>



<a href="shell.InitVariantFromDouble">InitVariantFromDouble</a>



<a href="shell.VariantToDoubleArray">VariantToDoubleArray</a>
 

 

