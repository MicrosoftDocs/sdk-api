---
UID: NF:propvarutil.VariantToDoubleArrayAlloc
title: VariantToDoubleArrayAlloc function
author: windows-sdk-content
description: Allocates an array of DOUBLE values then extracts data from a VARIANT structure into that array.
old-location: properties\VariantToDoubleArrayAlloc.htm
tech.root: properties
ms.assetid: 334d192e-7f63-47b4-88d4-9361e679cb15
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: VariantToDoubleArrayAlloc, VariantToDoubleArrayAlloc function [Windows Properties], _shell_VariantToDoubleArrayAlloc, properties.VariantToDoubleArrayAlloc, propvarutil/VariantToDoubleArrayAlloc, shell.VariantToDoubleArrayAlloc
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
 - VariantToDoubleArrayAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToDoubleArrayAlloc function


## -description


Allocates an array of <b>DOUBLE</b> values then extracts data from a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure into that array.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


### -param pprgn [out]

Type: <b>DOUBLE**</b>

When this function returns, contains a pointer to an array of <b>DOUBLE</b> values extracted from the source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains a pointer to the count of elements extracted from the source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used when the calling application expects a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> to hold an array of <b>DOUBLE</b> values.

If the source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> is of type VT_ARRAY | VT_R8, this function extracts an array of <b>DOUBLE</b> values into a newly allocated array. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the array pointed to by <i>pprgn</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToDoubleArrayAlloc">VariantToDoubleArrayAlloc</a> to access a <b>DOUBLE</b> array value in a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a>.


```cpp
// VARIANT var;
// Assume variable var is initialized and valid.
// The application expects var to contain an array of DOUBLE values.
DOUBLE *prgDoubles;
ULONG cElems;

HRESULT hr = VariantToDoubleArrayAlloc(var, &prgDoubles, &cElems);

if (SUCCEEDED(hr))
{
     // prgDoubles now points to a vector of cElems DOUBLEs.
     CoTaskMemFree(prgDoubles);
}
```





## -see-also




<a href="shell.InitVariantFromDoubleArray">InitVariantFromDoubleArray</a>



<a href="shell.PropVariantChangeType">PropVariantChangeType</a>



<a href="shell.PropVariantToDoubleVectorAlloc">PropVariantToDoubleVectorAlloc</a>



<a href="shell.VariantToDoubleArray">VariantToDoubleArray</a>
 

 

