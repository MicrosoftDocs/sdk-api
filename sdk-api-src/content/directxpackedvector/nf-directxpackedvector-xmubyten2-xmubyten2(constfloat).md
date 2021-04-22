---
UID: NF:directxpackedvector.XMUBYTEN2.XMUBYTEN2(constfloat)
title: XMUBYTEN2::XMUBYTEN2(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTEN2 from a two-element float array argument.
helpviewer_keywords: ["XMUBYTEN2","XMUBYTEN2 constructor [DirectX Math Support APIs]","XMUBYTEN2 constructor [DirectX Math Support APIs]","XMUBYTEN2 structure","XMUBYTEN2 structure [DirectX Math Support APIs]","XMUBYTEN2 constructor","XMUBYTEN2.XMUBYTEN2","XMUBYTEN2.XMUBYTEN2()","XMUBYTEN2.XMUBYTEN2(const float)","XMUBYTEN2::XMUBYTEN2","XMUBYTEN2::XMUBYTEN2(const float)","dxmath.xmubyten2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 2063bde1-65f3-4962-8846-5eda52da8baa
ms.date: 05/06/2019
ms.keywords: XMUBYTEN2, XMUBYTEN2 constructor [DirectX Math Support APIs], XMUBYTEN2 constructor [DirectX Math Support APIs],XMUBYTEN2 structure, XMUBYTEN2 structure [DirectX Math Support APIs],XMUBYTEN2 constructor, XMUBYTEN2.XMUBYTEN2, XMUBYTEN2.XMUBYTEN2(), XMUBYTEN2.XMUBYTEN2(const float), XMUBYTEN2::XMUBYTEN2, XMUBYTEN2::XMUBYTEN2(const float), dxmath.xmubyten2_ctor_1
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

# XMUBYTEN2::XMUBYTEN2(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten2">XMUBYTEN2</a> from a two-element <code>float</code> array argument.

This constructor initializes a new instance of **XMUBYTEN2** from a from a two-element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available with C++.</div>

## -parameters

### -param pArray

Two-element **float** array containing the values used to initialize the two components of a new instance of **XMUBYTEN2**.

## -remarks

| Vector Component | Array Element | Range | Description |
|------------------|---------------|-------|--|
| x | pArray[0] | 0.0, 1.0 | During instantiation, pArray[0] is clamped between 0 and 1, multiplied by 255.0f and assigned to x. |
| y | pArray[1] | 0.0, 1.0 | During instantiation, pArray[1] is clamped between 0 and 1, multiplied by 255.0f, and then assigned to y. |

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTEN2 instance;
_x1=min( max( pArray[0], 0.0 ), 1.0 );
_y1=min( max( pArray[1], 0.0 ), 1.0 );
_x1 = round( _x1 *  255.0f);
_y1 = round( _y1 *  255.0f);
instance.x = (uint8_t)_x1;
instance.y = (uint8_t)_y1;
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten2">XMUBYTEN2</a>

<a href="/windows/desktop/dxmath/xmubyten2-ctor">XMUBYTEN2 Constructors</a>