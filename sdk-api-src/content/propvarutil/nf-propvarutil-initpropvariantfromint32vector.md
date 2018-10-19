---
UID: NF:propvarutil.InitPropVariantFromInt32Vector
title: InitPropVariantFromInt32Vector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a vector of 32-bit integer values.
old-location: properties\InitPropVariantFromInt32Vector.htm
tech.root: properties
ms.assetid: 67173750-7b76-47fc-aec3-7e4e39a73532
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: InitPropVariantFromInt32Vector, InitPropVariantFromInt32Vector function [Windows Properties], properties.InitPropVariantFromInt32Vector, propvarutil/InitPropVariantFromInt32Vector, shell.InitPropVariantFromInt32Vector, shell_InitPropVariantFromInt32Vector
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
 - InitPropVariantFromInt32Vector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromInt32Vector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a vector of 32-bit integer values.


## -parameters




### -param prgn [in]

Type: <b>const LONG*</b>

Pointer to a source vector of <b>LONG</b> values. If this parameter is <b>NULL</b>, the vector is initialized with zeros.


### -param cElems [in]

Type: <b>ULONG</b>

The number of vector elements.


### -param ppropvar [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_VECTOR | VT_I4 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromInt32Vector">InitPropVariantFromInt32Vector</a>.


```cpp
LONG rgLongs[] = {1, 2, 7};
PROPVARIANT propvar;

HRESULT hr = InitPropVariantFromInt32Vector(rgLongs, ARRAYSIZE(rgLongs), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_I4.
 
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="shell.InitPropVariantFromInt32">InitPropVariantFromInt32</a>



<a href="shell.InitVariantFromInt32">InitVariantFromInt32</a>



<a href="shell.PropVariantToInt32Vector">PropVariantToInt32Vector</a>
 

 

