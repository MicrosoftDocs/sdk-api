---
UID: NF:directxpackedvector.XMUNIBBLE4.XMUNIBBLE4(constfloat)
title: XMUNIBBLE4::XMUNIBBLE4(const float) (directxpackedvector.h)
description: Initializes a new instance of **XMUNIBBLE4** from a four element float array argument.
helpviewer_keywords: ["XMUNIBBLE4","XMUNIBBLE4 constructor [DirectX Math Support APIs]","XMUNIBBLE4 constructor [DirectX Math Support APIs]","XMUNIBBLE4 structure","XMUNIBBLE4 structure [DirectX Math Support APIs]","XMUNIBBLE4 constructor","XMUNIBBLE4.XMUNIBBLE4","XMUNIBBLE4.XMUNIBBLE4()","XMUNIBBLE4.XMUNIBBLE4(const float)","XMUNIBBLE4::XMUNIBBLE4","XMUNIBBLE4::XMUNIBBLE4(const float)","dxmath.xmunibble4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 0ea8d7fa-2600-44eb-8d6a-a36364f98f17
ms.date: 05/06/2019
ms.keywords: XMUNIBBLE4, XMUNIBBLE4 constructor [DirectX Math Support APIs], XMUNIBBLE4 constructor [DirectX Math Support APIs],XMUNIBBLE4 structure, XMUNIBBLE4 structure [DirectX Math Support APIs],XMUNIBBLE4 constructor, XMUNIBBLE4.XMUNIBBLE4, XMUNIBBLE4.XMUNIBBLE4(), XMUNIBBLE4.XMUNIBBLE4(const float), XMUNIBBLE4::XMUNIBBLE4, XMUNIBBLE4::XMUNIBBLE4(const float), dxmath.xmunibble4_ctor_1
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
 - XMUNIBBLE4::XMUNIBBLE4
 - directxpackedvector/XMUNIBBLE4::XMUNIBBLE4
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
 - XMUNIBBLE4.XMUNIBBLE4
---

# XMUNIBBLE4::XMUNIBBLE4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of XMUNIBBLE4 from a from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This is only available for C++ based development.</div>

## -parameters

### -param pArray

Four element floating point array containing the values used to initialize the four components of a new instance of **XMUNIBBLE4**.

## -remarks

Array elements are mapped to the vector components of a new instance of **XMUNIBBLE4** as follows:

| XMUNIBBLE4 Member | Array Element | Range |
|---------------|----------|-------|
| x | pArray[0] | 0.0, 15.0 |
| y | pArray[1] | 0.0, 15.0 |
| z | pArray[2] | 0.0, 15.0 |
| w | pArray[3] | 0.0, 15.0 |

Elements of *pArray* will be clamped to the permitted range prior to assignment to the appropriate member of **XMUNIBBLE4**.

The following pseudocode demonstrates the operation of this constructor, which takes advantage of the union of the four components of the **XMUNIBBLE4** vector with an instance of **uint16_t** in the definition of the structure:

```cpp
XMUNIBBLE4 instance;
_x1=min( max( pArray[0], 0 ), 15.0 );
_y1=min( max( pArray[1], 0 ), 15.0 );
_z1=min( max( pArray[2], 0 ), 15.0 );
_w1=min( max( pArray[3], 0 ), 15.0 );

instance.v =  ( (uint16_t)_w1 << 12) |
                (((uint16_t)_z1 & 0xF) << 8) |
                (((uint16_t)_y1 & 0xF) << 4) |
                (((uint16_t)_x1 & 0xF));
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmunibble4">XMUNIBBLE4</a>

<a href="/windows/desktop/dxmath/xmunibble4-ctor">XMUNIBBLE4 Constructors</a>