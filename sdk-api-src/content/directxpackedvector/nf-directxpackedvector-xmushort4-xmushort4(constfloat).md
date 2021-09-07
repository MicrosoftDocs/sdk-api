---
UID: NF:directxpackedvector.XMUSHORT4.XMUSHORT4(constfloat)
title: XMUSHORT4::XMUSHORT4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUSHORT4 from a four element float array argument.
helpviewer_keywords: ["XMUSHORT4","XMUSHORT4 constructor [DirectX Math Support APIs]","XMUSHORT4 constructor [DirectX Math Support APIs]","XMUSHORT4 structure","XMUSHORT4 structure [DirectX Math Support APIs]","XMUSHORT4 constructor","XMUSHORT4.XMUSHORT4","XMUSHORT4.XMUSHORT4()","XMUSHORT4.XMUSHORT4(const float)","XMUSHORT4::XMUSHORT4","XMUSHORT4::XMUSHORT4(const float)","dxmath.xmushort4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: dc92c135-7775-4ce8-b3b8-396dfe2cf81f
ms.date: 05/06/2019
ms.keywords: XMUSHORT4, XMUSHORT4 constructor [DirectX Math Support APIs], XMUSHORT4 constructor [DirectX Math Support APIs],XMUSHORT4 structure, XMUSHORT4 structure [DirectX Math Support APIs],XMUSHORT4 constructor, XMUSHORT4.XMUSHORT4, XMUSHORT4.XMUSHORT4(), XMUSHORT4.XMUSHORT4(const float), XMUSHORT4::XMUSHORT4, XMUSHORT4::XMUSHORT4(const float), dxmath.xmushort4_ctor_1
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
 - XMUSHORT4::XMUSHORT4
 - directxpackedvector/XMUSHORT4::XMUSHORT4
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
 - XMUSHORT4.XMUSHORT4
---

# XMUSHORT4::XMUSHORT4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort4">XMUSHORT4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMUSHORT4** from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element **float** array containing the values used to initialize the four components of a new instance of **XMUSHORT4**.

## -remarks

The magnitude of each member of the *pArray* argument to the constructor will be clamped to the range supported by a 16-bit signed integer [0, 65535.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUSHORT4 instance;

instance.x = (uint16_t)min( max( pArray[0] 0.0 ), 65535.0 );
instance.y = (uint16_t)min( max( pArray[1] 0.0 ), 65535.0 );
instance.z = (uint16_t)min( max( pArray[2] 0.0 ), 65535.0 );
instance.w = (uint16_t)min( max( pArray[3] 0.0 ), 65535.0 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort4">XMUSHORT4</a>

<a href="/windows/desktop/dxmath/xmushort4-ctor">XMUSHORT4 Constructors</a>