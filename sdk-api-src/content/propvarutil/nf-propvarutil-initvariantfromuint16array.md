---
UID: NF:propvarutil.InitVariantFromUInt16Array
title: InitVariantFromUInt16Array function
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of unsigned 16-bit integer values.
old-location: properties\InitVariantFromUInt16Array.htm
old-project: properties
ms.assetid: 57fe1dd2-48a5-486e-a2cb-53cf0b8f96b0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: InitVariantFromUInt16Array, InitVariantFromUInt16Array function [Windows Properties], _shell_InitVariantFromUInt16Array, properties.InitVariantFromUInt16Array, propvarutil/InitVariantFromUInt16Array, shell.InitVariantFromUInt16Array
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
 - InitVariantFromUInt16Array
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# InitVariantFromUInt16Array function


## -description


Initializes a <a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a> structure with an array of unsigned 16-bit integer values.


## -parameters




### -param prgn [in]

Type: <b>const USHORT*</b>

Pointer to the source array of <b>USHORT</b> values.


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



Creates a VT_ARRAY | VT_UI2 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/library/Bb762339(v=VS.85).aspx">InitVariantFromUInt16Array</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>USHORT rgShorts[] = {3, 1};
VARIANT var;

HRESULT hr = InitVariantFromUInt16Array(rgShorts, ARRAYSIZE(rgShorts), &amp;var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_UI2.
    VariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/library/Bb762310(v=VS.85).aspx">InitPropVariantFromUInt16Vector</a>



<a href="https://msdn.microsoft.com/library/Bb762338(v=VS.85).aspx">InitVariantFromUInt16</a>



<a href="https://msdn.microsoft.com/library/Bb776624(v=VS.85).aspx">VariantToUInt16Array</a>
 

 

