---
UID: NF:propvarutil.ClearPropVariantArray
title: ClearPropVariantArray function (propvarutil.h)
description: Frees the memory and references used by an array of PROPVARIANT structures stored in an array.
helpviewer_keywords: ["ClearPropVariantArray","ClearPropVariantArray function [Windows Properties]","_shell_ClearPropVariantArray","properties.ClearPropVariantArray","propvarutil/ClearPropVariantArray","shell.ClearPropVariantArray"]
old-location: properties\ClearPropVariantArray.htm
tech.root: properties
ms.assetid: e8d7f951-8a9e-441b-9fa7-bf21cf08c8ac
ms.date: 12/05/2018
ms.keywords: ClearPropVariantArray, ClearPropVariantArray function [Windows Properties], _shell_ClearPropVariantArray, properties.ClearPropVariantArray, propvarutil/ClearPropVariantArray, shell.ClearPropVariantArray
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - ClearPropVariantArray
 - propvarutil/ClearPropVariantArray
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - ClearPropVariantArray
---

# ClearPropVariantArray function


## -description

Frees the memory and references used by an array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures stored in an array.

## -parameters

### -param rgPropVar [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

Array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures to free.

### -param cVars [in]

Type: <b>UINT</b>

The number of elements in the array specified by <i>rgPropVar</i>.

## -returns

No return value.

## -remarks

This function releases the memory and references held by each structure in the array before setting the structures to zero.

This function performs the same action as <a href="/windows/desktop/api/propidl/nf-propidl-freepropvariantarray">FreePropVariantArray</a>, but <b>FreePropVariantArray</b> returns an <b>HRESULT</b>.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-clearpropvariantarray">ClearPropVariantArray</a>



```cpp
// PROPVARIANT rgpropvar[5];
// Assume all 5 propvariants are initialized and valid.

ClearPropVariantArray(rgpropvar, ARRAYSIZE(rgpropvar));
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-clearvariantarray">ClearVariantArray</a>