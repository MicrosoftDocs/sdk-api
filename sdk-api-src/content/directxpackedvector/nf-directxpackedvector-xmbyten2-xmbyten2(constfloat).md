---
UID: NF:directxpackedvector.XMBYTEN2.XMBYTEN2(constfloat)
title: XMBYTEN2::XMBYTEN2(const float) (directxpackedvector.h)
description: Initializes a new instance of XMBYTEN2 from a two-element float array argument.
helpviewer_keywords: ["XMBYTEN2","XMBYTEN2 constructor [DirectX Math Support APIs]","XMBYTEN2 constructor [DirectX Math Support APIs]","XMBYTEN2 structure","XMBYTEN2 structure [DirectX Math Support APIs]","XMBYTEN2 constructor","XMBYTEN2.XMBYTEN2","XMBYTEN2.XMBYTEN2()","XMBYTEN2.XMBYTEN2(const float)","XMBYTEN2::XMBYTEN2","XMBYTEN2::XMBYTEN2(const float)","dxmath.xmbyten2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 5d6b2f0e-fa41-46ff-9418-c11246bdb266
ms.date: 05/06/2019
ms.keywords: XMBYTEN2, XMBYTEN2 constructor [DirectX Math Support APIs], XMBYTEN2 constructor [DirectX Math Support APIs],XMBYTEN2 structure, XMBYTEN2 structure [DirectX Math Support APIs],XMBYTEN2 constructor, XMBYTEN2.XMBYTEN2, XMBYTEN2.XMBYTEN2(), XMBYTEN2.XMBYTEN2(const float), XMBYTEN2::XMBYTEN2, XMBYTEN2::XMBYTEN2(const float), dxmath.xmbyten2_ctor_1
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
 - XMBYTEN2::XMBYTEN2
 - directxpackedvector/XMBYTEN2::XMBYTEN2
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
 - XMBYTEN2.XMBYTEN2
---

# XMBYTEN2::XMBYTEN2(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten2">XMBYTEN2</a> from a two-element <code>float</code> array argument.

This constructor initializes a new instance of **XMBYTEN2** from a two-element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available with C++.</div>

## -parameters

### -param pArray

Two-element <code>float</code> array containing the values used to initialize the two components of a new instance of **XMBYTEN2**.

## -remarks

| Vector Component | Array Element | Range | Description |
|-----------------|----------------|-------|-|
| x | pArray[0] | -1.0, 1.0 | During instantiation, pArray[0] is clamped between -1 and 1, multiplied by 127.0f and assigned to x. |
| y | pArray[1] | -1.0, 1.0 | During instantiation, pArray[1] is clamped between -1 and 1, multiplied by 127.0f, and then assigned to y. |

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMBYTEN2 instance;
_x1=min( max( pArray[0], -1.0 ), 1.0 );
_y1=min( max( pArray[1], -1.0 ), 1.0 );
_x1 = round( _x1 *  127.0f);
_y1 = round( _y1 *  127.0f);
instance.x = (int8_t)_x1;
instance.y = (int8_t)_y1;
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyten2">XMBYTEN2</a>

<a href="/windows/desktop/dxmath/xmbyten2-ctor">XMBYTEN2 Constructors</a>