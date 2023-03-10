---
UID: NF:directxpackedvector.XMUBYTEN4.XMUBYTEN4(constfloat)
title: XMUBYTEN4::XMUBYTEN4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTEN4 from a four element float array argument.
helpviewer_keywords: ["XMUBYTEN4","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 structure","XMUBYTEN4 structure [DirectX Math Support APIs]","XMUBYTEN4 constructor","XMUBYTEN4.XMUBYTEN4","XMUBYTEN4.XMUBYTEN4()","XMUBYTEN4.XMUBYTEN4(const float)","XMUBYTEN4::XMUBYTEN4","XMUBYTEN4::XMUBYTEN4(const float)","dxmath.xmubyten4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 0b4ee605-ef9d-458b-af9a-83f27c9f4cb5
ms.date: 05/06/2019
ms.keywords: XMUBYTEN4, XMUBYTEN4 constructor [DirectX Math Support APIs], XMUBYTEN4 constructor [DirectX Math Support APIs],XMUBYTEN4 structure, XMUBYTEN4 structure [DirectX Math Support APIs],XMUBYTEN4 constructor, XMUBYTEN4.XMUBYTEN4, XMUBYTEN4.XMUBYTEN4(), XMUBYTEN4.XMUBYTEN4(const float), XMUBYTEN4::XMUBYTEN4, XMUBYTEN4::XMUBYTEN4(const float), dxmath.xmubyten4_ctor_1
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
 - XMUBYTEN4::XMUBYTEN4
 - directxpackedvector/XMUBYTEN4::XMUBYTEN4
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
 - XMUBYTEN4.XMUBYTEN4
---

# XMUBYTEN4::XMUBYTEN4(const float)


## -description

Initializes a new instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMUBYTEN4** from a from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element **float** array containing the values used to initialize the four components of a new instance of **XMUBYTEN4**.

## -remarks

| Vector Component | Array Element | Range | Description |
|------------------|---------------|-------|--|
| x | pArray[0] | 0.0, 1.0 | During instantiation, pArray[0] is clamped between 0 and 1, multiplied by 255.0f and assigned to x. |
| y | pArray[1] | 0.0, 1.0 | During instantiation, pArray[1] is clamped between 0 and 1, multiplied by 255.0f, and then assigned to y. |
| z | pArray[2] | 0.0, 1.0 | During instantiation, pArray[2] is clamped between 0 and 1, multiplied by 255.0f, and then assigned to z. |
| w | pArray[3] | 0.0, 1.0 | During instantiation, pArray[3] is clamped between 0 and 1, multiplied by 255.0f, and then assigned to w. |

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTEN4 instance;
_x1=min( max( pArray[0], 0.0 ), 1.0 );
_y1=min( max( pArray[1], 0.0 ), 1.0 );
_z1=min( max( pArray[2], 0.0 ), 1.0 );
_w1=min( max( pArray[3], 0.0 ), 1.0 );
_x1 = round( _x1 *  255.0f);
_y1 = round( _y1 *  255.0f);
_z1 = round( _z1 *  255.0f);
_w1 = round( _w1 *  255.0f);
instance.x = (uint8_t)_x1;
instance.y = (uint8_t)_y1;
instance.z = (uint8_t)_z1;
instance.w = (uint8_t)_w1;
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a>

<a href="/windows/desktop/dxmath/xmubyten4-ctor">XMUBYTEN4 Constructors</a>
