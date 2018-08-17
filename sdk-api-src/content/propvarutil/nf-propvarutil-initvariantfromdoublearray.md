---
UID: NF:propvarutil.InitVariantFromDoubleArray
title: InitVariantFromDoubleArray function
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of values of type DOUBLE.
old-location: properties\InitVariantFromDoubleArray.htm
old-project: properties
ms.assetid: 781b6999-4551-499d-ba37-0a7e05fc6eab
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitVariantFromDoubleArray, InitVariantFromDoubleArray function [Windows Properties], _shell_InitVariantFromDoubleArray, properties.InitVariantFromDoubleArray, propvarutil/InitVariantFromDoubleArray, shell.InitVariantFromDoubleArray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 - InitVariantFromDoubleArray
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitVariantFromDoubleArray function


## -description


Initializes a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure with an array of values of type DOUBLE.


## -parameters




### -param prgn [in]

Type: <b>const DOUBLE*</b>

Pointer to the source array of DOUBLE values.


### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgn</i>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_ARRAY | VT_R8 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762322(v=VS.85).aspx">InitVariantFromDoubleArray</a>.

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




<a href="https://msdn.microsoft.com/en-us/library/Bb762292(v=VS.85).aspx">InitPropVariantFromDoubleVector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762321(v=VS.85).aspx">InitVariantFromDouble</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776599(v=VS.85).aspx">VariantToDoubleArray</a>
 

 

