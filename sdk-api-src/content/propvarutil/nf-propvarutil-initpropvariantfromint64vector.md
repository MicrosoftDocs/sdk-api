---
UID: NF:propvarutil.InitPropVariantFromInt64Vector
title: InitPropVariantFromInt64Vector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a vector of Int64 values.
old-location: properties\InitPropVariantFromInt64Vector.htm
tech.root: properties
ms.assetid: a2375776-ba9e-4d59-8924-86ac087b99d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InitPropVariantFromInt64Vector, InitPropVariantFromInt64Vector function [Windows Properties], properties.InitPropVariantFromInt64Vector, propvarutil/InitPropVariantFromInt64Vector, shell.InitPropVariantFromInt64Vector, shell_InitPropVariantFromInt64Vector
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
 - InitPropVariantFromInt64Vector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromInt64Vector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a vector of <b>Int64</b> values.


## -parameters




### -param prgn [in]

Type: <b>const LONGLONG*</b>

Pointer to a source vector of <b>LONGLONG</b> values. If this parameter is <b>NULL</b>, the vector is initialized with zeros.


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



Creates a VT_VECTOR | VT_I8 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromInt64Vector">InitPropVariantFromInt64Vector</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>LONGLONG rgLongLongs[] = {4, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt64Vector(rgLongLongs, ARRAYSIZE(rgLongLongs), &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_I8.
 
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromInt64">InitPropVariantFromInt64</a>



<a href="shell.InitVariantFromInt64">InitVariantFromInt64</a>



<a href="shell.PropVariantToInt64Vector">PropVariantToInt64Vector</a>
 

 

