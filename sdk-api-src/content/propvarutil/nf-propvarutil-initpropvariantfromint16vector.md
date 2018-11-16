---
UID: NF:propvarutil.InitPropVariantFromInt16Vector
title: InitPropVariantFromInt16Vector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a specified vector of 16-bit integer values.
old-location: properties\InitPropVariantFromInt16Vector.htm
tech.root: properties
ms.assetid: 487204af-152e-4e39-808f-492dae7cadee
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: InitPropVariantFromInt16Vector, InitPropVariantFromInt16Vector function [Windows Properties], properties.InitPropVariantFromInt16Vector, propvarutil/InitPropVariantFromInt16Vector, shell.InitPropVariantFromInt16Vector, shell_InitPropVariantFromInt16Vector
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
 - InitPropVariantFromInt16Vector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitPropVariantFromInt16Vector
: 
---

# InitPropVariantFromInt16Vector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a specified vector of 16-bit integer values.


## -parameters




### -param prgn [in]

Type: <b>const SHORT*</b>

Pointer to a source vector of <b>SHORT</b> values. If this parameter is <b>NULL</b>, the vector is initialized with zeros.


### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the vector.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_VECTOR | VT_I2 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762298(v=VS.85).aspx">InitPropVariantFromInt16Vector</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>SHORT rgShorts[] = {3, 1, 4};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt16Vector(rgShorts, ARRAYSIZE(rgShorts), &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_I2.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762297(v=VS.85).aspx">InitPropVariantFromInt16</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762327(v=VS.85).aspx">InitVariantFromInt16</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776547(v=VS.85).aspx">PropVariantToInt16Vector</a>
 

 

