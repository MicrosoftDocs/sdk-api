---
UID: NF:propvarutil.InitPropVariantFromUInt64Vector
title: InitPropVariantFromUInt64Vector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a vector of 64-bit unsigned integers.
old-location: properties\InitPropVariantFromUInt64Vector.htm
tech.root: properties
ms.assetid: 17c52a7d-c3d3-4132-8f44-7d0b250aa7ad
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitPropVariantFromUInt64Vector, InitPropVariantFromUInt64Vector function [Windows Properties], properties.InitPropVariantFromUInt64Vector, propvarutil/InitPropVariantFromUInt64Vector, shell.InitPropVariantFromUInt64Vector, shell_InitPropVariantFromUInt64Vector
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
 - InitPropVariantFromUInt64Vector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromUInt64Vector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a vector of 64-bit unsigned integers.


## -parameters




### -param prgn [in]

Type: <b>const ULONGLONG*</b>

Pointer to a source vector of <b>ULONGLONG</b> values. If this parameter is <b>NULL</b>, the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> is initialized with zeros.


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



Creates a VT_VECTOR | VT_UI8 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromUInt64Vector">InitPropVariantFromUInt64Vector</a>.


```cpp
ULONGLONG rgLongs[] = {4, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromUInt32Vector(rgLongs, ARRAYSIZE(rgLongs), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_UI8.
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="shell.InitPropVariantFromUInt64">InitPropVariantFromUInt64</a>



<a href="shell.InitVariantFromUInt64Array">InitVariantFromUInt64Array</a>



<a href="shell.PropVariantToUInt64Vector">PropVariantToUInt64Vector</a>
 

 

