---
UID: NF:directxpackedvector.XMUBYTEN2.XMUBYTEN2(constuint8_t)
title: XMUBYTEN2::XMUBYTEN2(const uint8_t) (directxpackedvector.h)
description: Default constructor for XMUBYTEN2. (overload 1/2)
helpviewer_keywords: ["XMUBYTEN2","XMUBYTEN2 constructor [DirectX Math Support APIs]","XMUBYTEN2 constructor [DirectX Math Support APIs]","XMUBYTEN2 structure","XMUBYTEN2 structure [DirectX Math Support APIs]","XMUBYTEN2 constructor","XMUBYTEN2.XMUBYTEN2","XMUBYTEN2.XMUBYTEN2()","XMUBYTEN2.XMUBYTEN2(const uint8_t)","XMUBYTEN2::XMUBYTEN2","XMUBYTEN2::XMUBYTEN2(const uint8_t)","dxmath.xmubyten2_ctor_1"]
old-location: Initializes a new instance of XMUBYTEN2 from a two-element uint8_t array argument.
tech.root: dxmath
ms.assetid: 7279d61f-209f-4b23-af9a-c10d56da8230
ms.date: 05/06/2019
ms.keywords: XMUBYTEN2, XMUBYTEN2 constructor [DirectX Math Support APIs], XMUBYTEN2 constructor [DirectX Math Support APIs],XMUBYTEN2 structure, XMUBYTEN2 structure [DirectX Math Support APIs],XMUBYTEN2 constructor, XMUBYTEN2.XMUBYTEN2, XMUBYTEN2.XMUBYTEN2(), XMUBYTEN2.XMUBYTEN2(const uint8_t), XMUBYTEN2::XMUBYTEN2, XMUBYTEN2::XMUBYTEN2(const uint8_t), dxmath.xmubyten2_ctor_1
req.header: directxpackedvector.h
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
req.namespace: DirectX::PackedVector
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
 - XMUBYTEN2::XMUBYTEN2
 - directxpackedvector/XMUBYTEN2::XMUBYTEN2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXPackedVector.h
api_name:
 - XMUBYTEN2.XMUBYTEN2
---

# XMUBYTEN2::XMUBYTEN2(const uint8_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten2">XMUBYTEN2</a> from a two-element <code>uint8_t</code> array argument.

This constructor initializes a new instance of **XMUBYTEN2** from a two-element <code>uint8_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available with C++.</div>

## -parameters

### -param pArray

Two-element *uint8_t* array containing the values used to initialize the two components of a new instance of **XMUBYTEN2**.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTEN2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten2">XMUBYTEN2</a>

<a href="/windows/desktop/dxmath/xmubyten2-ctor">XMUBYTEN2 Constructors</a>
