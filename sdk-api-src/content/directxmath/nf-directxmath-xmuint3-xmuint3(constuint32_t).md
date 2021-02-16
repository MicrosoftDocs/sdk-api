---
UID: NF:directxmath.XMUINT3.XMUINT3(constuint32_t)
title: XMUINT3::XMUINT3(const uint32_t) (directxmath.h)
description: Initializes a new instance of XMUINT3 from a three element uint32_t array argument.
helpviewer_keywords: ["XMUINT3","XMUINT3 constructor [DirectX Math Support APIs]","XMUINT3 constructor [DirectX Math Support APIs]","XMUINT3 structure","XMUINT3 structure [DirectX Math Support APIs]","XMUINT3 constructor","XMUINT3.XMUINT3","XMUINT3.XMUINT3()","XMUINT3.XMUINT3(const uint32_t)","XMUINT3::XMUINT3","XMUINT3::XMUINT3(const uint32_t)","dxmath.xmuint3_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 44e21d02-43b9-4148-ba63-3440c0954860
ms.date: 05/13/2019
ms.keywords: XMUINT3, XMUINT3 constructor [DirectX Math Support APIs], XMUINT3 constructor [DirectX Math Support APIs],XMUINT3 structure, XMUINT3 structure [DirectX Math Support APIs],XMUINT3 constructor, XMUINT3.XMUINT3, XMUINT3.XMUINT3(), XMUINT3.XMUINT3(const uint32_t), XMUINT3::XMUINT3, XMUINT3::XMUINT3(const uint32_t), dxmath.xmuint3_ctor_1
req.header: directxmath.h
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
req.namespace: Use DirectX.
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - XMUINT3::XMUINT3
 - directxmath/XMUINT3::XMUINT3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMUINT3.XMUINT3
---

# XMUINT3::XMUINT3(const uint32_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint3">XMUINT3</a> from a three element <code>uint32_t</code> array argument.

This constructor initializes a new instance of **XMUINT3** from a three-element <code>uint32_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Three-element **uint32_t** array containing the values used to initialize the three components of a new instance of **XMUINT3**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUINT3 instance;
instance.x =  pArray[0];
instance.y =  pArray[1];
instance.z =  pArray[2];
```

## -see-also

<a href="/windows/desktop/api/directxmath/ns-directxmath-xmuint3">XMUINT3</a>

<a href="/windows/desktop/api/directxmath/nf-directxmath-xmuint3-xmuint3(constuint32_t)">XMUINT3 Constructors</a>