---
UID: NF:propvarutil.InitVariantFromDoubleArray
title: InitVariantFromDoubleArray function (propvarutil.h)
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of values of type DOUBLE.
old-location: properties\InitVariantFromDoubleArray.htm
tech.root: properties
ms.assetid: 781b6999-4551-499d-ba37-0a7e05fc6eab
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitVariantFromDoubleArray, InitVariantFromDoubleArray function [Windows Properties], _shell_InitVariantFromDoubleArray, properties.InitVariantFromDoubleArray, propvarutil/InitVariantFromDoubleArray, shell.InitVariantFromDoubleArray
ms.topic: function
f1_keywords: 
 - "propvarutil/InitVariantFromDoubleArray"
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
ms.custom: 19H1
---

# InitVariantFromDoubleArray function


## -description


Initializes a <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure with an array of values of type DOUBLE.


## -parameters




### -param prgn [in]

Type: <b>const DOUBLE*</b>

Pointer to the source array of DOUBLE values.


### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgn</i>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_ARRAY | VT_R8 variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromdoublearray">InitVariantFromDoubleArray</a>.


```cpp
DOUBLE rgDoubles[] = {34.7, 12.0};
VARIANT var;

HRESULT hr = InitVariantFromDoubleArray(rgDoubles, ARRAYSIZE(rgDoubles), &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_R8.
    VariantClear(&propvar);
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromdoublevector">InitPropVariantFromDoubleVector</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromdouble">InitVariantFromDouble</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-varianttodoublearray">VariantToDoubleArray</a>
 

 

