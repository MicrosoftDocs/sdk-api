---
UID: NF:propidl.FreePropVariantArray
title: FreePropVariantArray function (propidl.h)
description: Frees the memory and references used by an array of PROPVARIANT structures.
helpviewer_keywords: ["FreePropVariantArray","FreePropVariantArray function [Windows Properties]","_shell_FreePropVariantArray","properties.FreePropVariantArray","propidl/FreePropVariantArray","shell.FreePropVariantArray"]
old-location: properties\FreePropVariantArray.htm
tech.root: properties
ms.assetid: 5033557c-d43c-42b1-ae4e-0fb0569d697a
ms.date: 12/05/2018
ms.keywords: FreePropVariantArray, FreePropVariantArray function [Windows Properties], _shell_FreePropVariantArray, properties.FreePropVariantArray, propidl/FreePropVariantArray, shell.FreePropVariantArray
req.header: propidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ole32.lib
req.dll: Ole32.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - FreePropVariantArray
 - propidl/FreePropVariantArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-com-l1-1-3.dll
 - api-ms-win-core-com-l1-1-2.dll
 - Ole32.dll
 - API-MS-Win-Core-Com-l1-1-0.dll
 - ComBase.dll
 - API-MS-Win-Core-Com-l1-1-1.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-0.dll
 - API-MS-Win-DownLevel-Ole32-l1-1-1.dll
api_name:
 - FreePropVariantArray
---

# FreePropVariantArray function


## -description

Frees the memory and references used by an array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures.

## -parameters

### -param cVariants [in]

Type: <b>ULONG</b>

The number of elements in the array specified by <i>rgvars</i>.

### -param rgvars [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures to free. When this function successfully returns, the <b>PROPVARIANT</b> structures in the array are zeroed and their type is set to VT_EMPTY.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function releases the memory and references held by each structure in the array before setting the structures to zero.

This function performs the same action as <a href="/windows/desktop/api/propvarutil/nf-propvarutil-clearpropvariantarray">ClearPropVariantArray</a>, but returns an <b>HRESULT</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propidl/nf-propidl-freepropvariantarray">FreePropVariantArray</a>



```cpp
// PROPVARIANT rgpropvar[5];
// Assume all 5 propvariants are initialized and valid.

FreePropVariantArray(ARRAYSIZE(rgpropvar), rgpropvar);
```