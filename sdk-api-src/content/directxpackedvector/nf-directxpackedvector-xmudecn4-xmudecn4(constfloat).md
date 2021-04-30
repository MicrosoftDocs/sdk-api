---
UID: NF:directxpackedvector.XMUDECN4.XMUDECN4(constfloat)
title: XMUDECN4::XMUDECN4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUDECN4 from a four element float array argument.
helpviewer_keywords: ["XMUDECN4","XMUDECN4 constructor [DirectX Math Support APIs]","XMUDECN4 constructor [DirectX Math Support APIs]","XMUDECN4 structure","XMUDECN4 structure [DirectX Math Support APIs]","XMUDECN4 constructor","XMUDECN4.XMUDECN4","XMUDECN4.XMUDECN4()","XMUDECN4.XMUDECN4(const float)","XMUDECN4::XMUDECN4","XMUDECN4::XMUDECN4(const float)","dxmath.xmudecn4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 2aa7d74b-345d-4660-83ac-66fd5d46a6de
ms.date: 05/06/2019
ms.keywords: XMUDECN4, XMUDECN4 constructor [DirectX Math Support APIs], XMUDECN4 constructor [DirectX Math Support APIs],XMUDECN4 structure, XMUDECN4 structure [DirectX Math Support APIs],XMUDECN4 constructor, XMUDECN4.XMUDECN4, XMUDECN4.XMUDECN4(), XMUDECN4.XMUDECN4(const float), XMUDECN4::XMUDECN4, XMUDECN4::XMUDECN4(const float), dxmath.xmudecn4_ctor_1
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
 - XMUDECN4::XMUDECN4
 - directxpackedvector/XMUDECN4::XMUDECN4
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
 - XMUDECN4.XMUDECN4
---

# XMUDECN4::XMUDECN4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudecn4">XMUDECN4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMUDECN4** from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element floating point array containing the values used to initialize the four components of a new instance of XMUDECN4.

## -remarks

Array elements are mapped to the vector components of a new instance of **XMUDECN4** as follows:

| Vector Component | Array Element | Range | Description |
|------------------|---------------|-------|--|
| x | pArray[0] | 0.0, 1.0 | During instantiation, pArray[0] is clamped between 0 and 1, multiplied by 1023.0f and assigned to **x**. |
| y | pArray[1] | 0.0, 1.0 | During instantiation, pArray[1] is clamped between 0 and 1, multiplied by 1023.0f, and then assigned to **y**. |
| z | pArray[2] | 0.0, 1.0 | During instantiation, pArray[2] is clamped between 0 and 1, multiplied by 1023.0f, and then assigned to **z**. |
| w | pArray[3] | 0.0, 1.0 | During instantiation, pArray[3] is clamped between 0 and 1, and then assigned to **w**. This argument should be between 0.0 and 1.0; during the instantiation of an instance of **XMUDECN4**, it is multiplied by 3.0f and then stored as the **w** member of the structure. |

```cpp
XMUDECN4 instance;
_x1=min( max( pArray[0], 0.0 ), 1.0 );
_y1=min( max( pArray[1], 0.0 ), 1.0 );
_z1=min( max( pArray[2], 0.0 ), 1.0 );
_w1=min( max( pArray[3], 0.0 ), 1.0 );
_x = round( _x *  1023.0f);
_y = round( _y *  1023.0f);
_z = round( _z *  1023.0f);
_w = round( _w *  3.0f);

instance.v =  ( (uint32_t)_w1 << 30) |
                (((uint32_t)_z1 & 0x3FF) << 20) |
                (((uint32_t)_y1 & 0x3FF) << 10) |
                (((uint32_t)_x1 & 0x3FF));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmudecn4">XMUDECN4</a>

<a href="/windows/desktop/dxmath/xmudecn4-ctor">XMUDECN4 Constructors</a>