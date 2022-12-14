---
UID: NF:directxpackedvector.XMBYTEN4.XMBYTEN4(constfloat)
title: XMBYTEN4::XMBYTEN4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMBYTEN4 from a four element float array argument.
helpviewer_keywords: ["XMBYTEN4","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 constructor [DirectX Math Support APIs]","XMBYTEN4 structure","XMBYTEN4 structure [DirectX Math Support APIs]","XMBYTEN4 constructor","XMBYTEN4.XMBYTEN4","XMBYTEN4.XMBYTEN4()","XMBYTEN4.XMBYTEN4(const float)","XMBYTEN4::XMBYTEN4","XMBYTEN4::XMBYTEN4(const float)","dxmath.xmbyten4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 3700bc90-be64-4b80-87e5-7a08ae49b8a8
ms.date: 05/06/2019
ms.keywords: XMBYTEN4, XMBYTEN4 constructor [DirectX Math Support APIs], XMBYTEN4 constructor [DirectX Math Support APIs],XMBYTEN4 structure, XMBYTEN4 structure [DirectX Math Support APIs],XMBYTEN4 constructor, XMBYTEN4.XMBYTEN4, XMBYTEN4.XMBYTEN4(), XMBYTEN4.XMBYTEN4(const float), XMBYTEN4::XMBYTEN4, XMBYTEN4::XMBYTEN4(const float), dxmath.xmbyten4_ctor_1
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
 - XMBYTEN4::XMBYTEN4
 - directxpackedvector/XMBYTEN4::XMBYTEN4
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
 - XMBYTEN4.XMBYTEN4
---

# XMBYTEN4::XMBYTEN4(const float)


## -description

Initializes a new instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMBYTEN4** from a from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>float</code> array containing the values used to initialize the four components of a new instance of **XMBYTEN4**.

## -remarks

| Vector Component | Array Element | Range | Description |
|------------------|---------------|-------|-|
| x | pArray[0] | -1.0, 1.0 | During instantiation, pArray[0] is clamped between -1 and 1, multiplied by 127.0f and assigned to x. |
| y | pArray[1] | -1.0, 1.0 | During instantiation, pArray[1] is clamped between -1 and 1, multiplied by 127.0f, and then assigned to y. |
| z | pArray[2] | -1.0, 1.0 | During instantiation, pArray[2] is clamped between -1 and 1, multiplied by 127.0f, and then assigned to z. |
| w | pArray[3] | -1.0, 1.0 | During instantiation, pArray[3] is clamped between -1 and 1, multiplied by 127.0f, and then assigned to w. |

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMBYTEN4 instance;
_x1=min( max( pArray[0], -1.0 ), 1.0 );
_y1=min( max( pArray[1], -1.0 ), 1.0 );
_z1=min( max( pArray[2], -1.0 ), 1.0 );
_w1=min( max( pArray[3], -1.0 ), 1.0 );
_x1 = round( _x1 *  127.0f);
_y1 = round( _y1 *  127.0f);
_z1 = round( _z1 *  127.0f);
_w1 = round( _w1 *  127.0f);
instance.x = (int8_t)_x1;
instance.y = (int8_t)_y1;
instance.z = (int8_t)_z1;
instance.w = (int8_t)_w1;
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten4">XMBYTEN4</a>

<a href="/windows/desktop/dxmath/xmbyten4-ctor">XMBYTEN4 Constructors</a>
