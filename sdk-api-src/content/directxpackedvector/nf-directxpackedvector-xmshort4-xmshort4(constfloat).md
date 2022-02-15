---
UID: NF:directxpackedvector.XMSHORT4.XMSHORT4(constfloat)
title: XMSHORT4::XMSHORT4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMSHORT4 from a four element float array argument.
helpviewer_keywords: ["XMSHORT4","XMSHORT4 constructor [DirectX Math Support APIs]","XMSHORT4 constructor [DirectX Math Support APIs]","XMSHORT4 structure","XMSHORT4 structure [DirectX Math Support APIs]","XMSHORT4 constructor","XMSHORT4.XMSHORT4","XMSHORT4.XMSHORT4()","XMSHORT4.XMSHORT4(const float)","XMSHORT4::XMSHORT4","XMSHORT4::XMSHORT4(const float)","dxmath.xmshort4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: fc8e1211-9a6d-4407-8c08-a35895eb1af5
ms.date: 05/06/2019
ms.keywords: XMSHORT4, XMSHORT4 constructor [DirectX Math Support APIs], XMSHORT4 constructor [DirectX Math Support APIs],XMSHORT4 structure, XMSHORT4 structure [DirectX Math Support APIs],XMSHORT4 constructor, XMSHORT4.XMSHORT4, XMSHORT4.XMSHORT4(), XMSHORT4.XMSHORT4(const float), XMSHORT4::XMSHORT4, XMSHORT4::XMSHORT4(const float), dxmath.xmshort4_ctor_1
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
 - XMSHORT4::XMSHORT4
 - directxpackedvector/XMSHORT4::XMSHORT4
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
 - XMSHORT4.XMSHORT4
---

# XMSHORT4::XMSHORT4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMSHORT4** from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>float</code> array containing the values used to initialize the four components of a new instance of **XMSHORT4**.

## -remarks

The magnitude of each member of the *pArray* argument to the constructor will be clamped to the range supported by a 16-bit unsigned integer [-32767.0, 32767.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMSHORT4 instance;

instance.x = (int16_t)min( max( pArray[0] -32767.0 ), 32767.0 );
instance.y = (int16_t)min( max( pArray[1] -32767.0 ), 32767.0 );
instance.z = (int16_t)min( max( pArray[2] -32767.0 ), 32767.0 );
instance.w = (int16_t)min( max( pArray[3] -32767.0 ), 32767.0 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a>

<a href="/windows/desktop/dxmath/xmshort4-ctor">XMSHORT4 Constructors</a>