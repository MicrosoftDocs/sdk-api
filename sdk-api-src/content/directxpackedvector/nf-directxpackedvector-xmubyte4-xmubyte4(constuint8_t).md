---
UID: NF:directxpackedvector.XMUBYTE4.XMUBYTE4(constuint8_t)
title: XMUBYTE4::XMUBYTE4(const uint8_t) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTE4 from a four element float array argument.
helpviewer_keywords: ["XMUBYTE4","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 structure","XMUBYTE4 structure [DirectX Math Support APIs]","XMUBYTE4 constructor","XMUBYTE4.XMUBYTE4","XMUBYTE4.XMUBYTE4()","XMUBYTE4.XMUBYTE4(const uint8_t)","XMUBYTE4::XMUBYTE4","XMUBYTE4::XMUBYTE4(const uint8_t)","dxmath.xmubyte4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 5d279759-fda8-48f5-ab04-77c378c33889
ms.date: 05/06/2019
ms.keywords: XMUBYTE4, XMUBYTE4 constructor [DirectX Math Support APIs], XMUBYTE4 constructor [DirectX Math Support APIs],XMUBYTE4 structure, XMUBYTE4 structure [DirectX Math Support APIs],XMUBYTE4 constructor, XMUBYTE4.XMUBYTE4, XMUBYTE4.XMUBYTE4(), XMUBYTE4.XMUBYTE4(const uint8_t), XMUBYTE4::XMUBYTE4, XMUBYTE4::XMUBYTE4(const uint8_t), dxmath.xmubyte4_ctor_1
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
 - XMUBYTE4::XMUBYTE4
 - directxpackedvector/XMUBYTE4::XMUBYTE4
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
 - XMUBYTE4.XMUBYTE4
---

# XMUBYTE4::XMUBYTE4(const uint8_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of **XMUBYTE4** from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element **float** array containing the values used to initialize the four components of a new instance of **XMUBYTE4**.

## -remarks

The magnitude of each member of the *pArray* argument to the constructor will be clamped to the range supported by an 8-bit signed integer [0.0, 255.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTE4 instance;

instance.x = (uint8_t)min( max( pArray[0] 0.0 ), 255.0 );
instance.y = (uint8_t)min( max( pArray[1] 0.0 ), 255.0 );
instance.z = (uint8_t)min( max( pArray[2] 0.0 ), 255.0 );
instance.w = (uint8_t)min( max( pArray[3] 0.0 ), 255.0 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a>

<a href="/windows/desktop/dxmath/xmubyte4-ctor">XMUBYTE4 Constructors</a>