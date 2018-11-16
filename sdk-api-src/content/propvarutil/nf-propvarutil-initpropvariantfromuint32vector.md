---
UID: NF:propvarutil.InitPropVariantFromUInt32Vector
title: InitPropVariantFromUInt32Vector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a vector of 32-bit unsigned integer values.
old-location: properties\InitPropVariantFromUInt32Vector.htm
tech.root: properties
ms.assetid: 807793fc-c679-4749-816c-005a77a37f08
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: InitPropVariantFromUInt32Vector, InitPropVariantFromUInt32Vector function [Windows Properties], properties.InitPropVariantFromUInt32Vector, propvarutil/InitPropVariantFromUInt32Vector, shell.InitPropVariantFromUInt32Vector, shell_InitPropVariantFromUInt32Vector
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
 - InitPropVariantFromUInt32Vector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- InitPropVariantFromUInt32Vector
: 
---

# InitPropVariantFromUInt32Vector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a vector of 32-bit unsigned integer values.


## -parameters




### -param prgn [in]

Type: <b>const ULONG*</b>

Pointer to a source vector of <b>ULONG</b> values. If this parameter is <b>NULL</b>, the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> is initialized with zeros.


### -param cElems [in]

Type: <b>ULONG</b>

Number of elements in the vector pointed to by <i>prgn</i>.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_VECTOR | VT_UI4 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromUInt32Vector">InitPropVariantFromUInt32Vector</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>ULONG rgLongs[] = {4, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt32Vector(rgLongs, ARRAYSIZE(rgLongs), &amp;propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI4.
    PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromUInt32">InitPropVariantFromUInt32</a>



<a href="shell.InitVariantFromUInt32Array">InitVariantFromUInt32Array</a>



<a href="shell.PropVariantToUInt32Vector">PropVariantToUInt32Vector</a>
 

 

