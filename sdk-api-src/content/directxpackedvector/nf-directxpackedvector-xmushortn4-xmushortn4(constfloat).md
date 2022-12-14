---
UID: NF:directxpackedvector.XMUSHORTN4.XMUSHORTN4(constfloat)
title: XMUSHORTN4::XMUSHORTN4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUSHORTN4 from a four element float array argument.
helpviewer_keywords: ["XMUSHORTN4","XMUSHORTN4 constructor [DirectX Math Support APIs]","XMUSHORTN4 constructor [DirectX Math Support APIs]","XMUSHORTN4 structure","XMUSHORTN4 structure [DirectX Math Support APIs]","XMUSHORTN4 constructor","XMUSHORTN4.XMUSHORTN4","XMUSHORTN4.XMUSHORTN4()","XMUSHORTN4.XMUSHORTN4(const float)","XMUSHORTN4::XMUSHORTN4","XMUSHORTN4::XMUSHORTN4(const float)","dxmath.xmushortn4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: d9b1c62d-8201-4235-a532-9a0674fd1887
ms.date: 05/06/2019
ms.keywords: XMUSHORTN4, XMUSHORTN4 constructor [DirectX Math Support APIs], XMUSHORTN4 constructor [DirectX Math Support APIs],XMUSHORTN4 structure, XMUSHORTN4 structure [DirectX Math Support APIs],XMUSHORTN4 constructor, XMUSHORTN4.XMUSHORTN4, XMUSHORTN4.XMUSHORTN4(), XMUSHORTN4.XMUSHORTN4(const float), XMUSHORTN4::XMUSHORTN4, XMUSHORTN4::XMUSHORTN4(const float), dxmath.xmushortn4_ctor_1
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
 - XMUSHORTN4::XMUSHORTN4
 - directxpackedvector/XMUSHORTN4::XMUSHORTN4
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
 - XMUSHORTN4.XMUSHORTN4
---

# XMUSHORTN4::XMUSHORTN4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn4">XMUSHORTN4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMUSHORTN4** from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element floating point array containing the values used to initialize the four components of a new instance of **XMUSHORTN4**.

## -remarks

Array elements are mapped to the vector components of a new instance of **XMUSHORTN4** as follows:


| Vector Component | Array Element | Range | Description |
|------------------|---------------|-------|--|
| x | pArray[0] | 0.0, 1.0 | During instantiation, pArray[0] is clamped between 0 and 1, multiplied by 65535.0f and assigned to x. |
| y | pArray[1] | 0.0, 1.0 | During instantiation, pArray[1] is clamped between 0 and 1, multiplied by 65535.0f, and then assigned to y. |
| z | pArray[2] | 0.0, 1.0 | During instantiation, pArray[2] is clamped between 0 and 1, multiplied by 65535.0f, and then assigned to z. |
| w | pArray[3] | 0.0, 1.0 | During instantiation, pArray[3] is clamped between 0 and 1, multiplied by 65535.0f, and then assigned to w. |

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUSHORTN4 instance;
_x1=min( max( pArray[0], 0.0 ), 1.0 );
_y1=min( max( pArray[1], 0.0 ), 1.0 );
_z1=min( max( pArray[2], 0.0 ), 1.0 );
_w1=min( max( pArray[3], 0.0 ), 1.0 )
_x1 = round( _x1 * 65535.0f);
_y1 = round( _y1 * 65535.0f);
_z1 = round( _z1 * 65535.0f);
_w1 = round( _w1 * 65535.0f);
instance._x = _x1;
instance._y = _y1;
instance._z = _z1;
instance._w = _w1;
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn4">XMUSHORTN4</a>

<a href="/windows/desktop/dxmath/xmushortn4-ctor">XMUSHORTN4 Constructors</a>