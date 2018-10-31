---
UID: NF:propvarutil.InitPropVariantFromDoubleVector
title: InitPropVariantFromDoubleVector function
author: windows-sdk-content
description: Initializes a PROPVARIANT structure based on a specified vector of double values.
old-location: properties\InitPropVariantFromDoubleVector.htm
tech.root: properties
ms.assetid: 78e91213-870f-4bc1-b0eb-a9fbae3d6c4c
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: InitPropVariantFromDoubleVector, InitPropVariantFromDoubleVector function [Windows Properties], properties.InitPropVariantFromDoubleVector, propvarutil/InitPropVariantFromDoubleVector, shell.InitPropVariantFromDoubleVector, shell_InitPropVariantFromDoubleVector
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
 - InitPropVariantFromDoubleVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantFromDoubleVector function


## -description


Initializes a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure based on a specified vector of <b>double</b> values.


## -parameters




### -param prgn [in, optional]

Type: <b>const DOUBLE*</b>

Pointer to a <b>double</b> vector. If this value is <b>NULL</b>, the elements pointed to by the <b>cadbl.pElems</b> structure member are initialized with 0.0.


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



Creates a VT_VECTOR | VT_R8 propvariant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantFromDoubleVector">InitPropVariantFromDoubleVector</a>.


```cpp
PROPVARIANT propvar;
DOUBLE rgDouble[] = {3.1415, 42.7};

HRESULT hr = InitPropVariantFromDoubleVector(rgDouble, ARRAYSIZE(rgDouble), &propvar);

if (SUCCEEDED(hr))
{
    // propvar now is valid and has type VT_VECTOR | VT_R8.
 
    PropVariantClear(&propvar);
}
```





## -see-also




<a href="shell.InitPropVariantFromDouble">InitPropVariantFromDouble</a>



<a href="shell.InitVariantFromDoubleArray">InitVariantFromDoubleArray</a>



<a href="shell.PropVariantToDoubleVector">PropVariantToDoubleVector</a>
 

 

