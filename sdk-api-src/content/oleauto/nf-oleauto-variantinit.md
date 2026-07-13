---
UID: NF:oleauto.VariantInit
title: VariantInit function (oleauto.h)
description: Initializes a variant.
helpviewer_keywords: ["VariantInit","VariantInit function [Automation]","_oa96_VariantInit","automat.variantinit","oleauto/VariantInit"]
old-location: automat\variantinit.htm
tech.root: automat
ms.assetid: 96aeb671-5528-4d3c-8e70-313716550b42
ms.date: 12/05/2018
ms.keywords: VariantInit, VariantInit function [Automation], _oa96_VariantInit, automat.variantinit, oleauto/VariantInit
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VariantInit
 - oleauto/VariantInit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VariantInit
---

# VariantInit function


## -description

Initializes a variant.

## -parameters

### -param pvarg [out]

The variant to initialize.

## -remarks

The <b>VariantInit</b> function initializes the VARIANTARG by setting the <b>vt</b> field to VT_EMPTY. Unlike <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>, this function does not interpret the current contents of the VARIANTARG. Use <b>VariantInit</b> to initialize new local variables of type VARIANTARG (or VARIANT).


#### Examples

The following example shows how to initialize an array of variants, where <code>celt</code> is the number of elements in the array.


```cpp
for(int i = 0; i < celt; ++i)
   VariantInit(&rgvar[i]);
```

## -see-also

<a href="/previous-versions/windows/desktop/automat/variant-manipulation-functions">Variant Manipulation Functions</a>
