---
UID: NF:directxpackedvector.XMBYTE4.XMBYTE4(constfloat)
title: XMBYTE4::XMBYTE4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMBYTE4 from a four element float array argument.
helpviewer_keywords: ["XMBYTE4","XMBYTE4 constructor [DirectX Math Support APIs]","XMBYTE4 constructor [DirectX Math Support APIs]","XMBYTE4 structure","XMBYTE4 structure [DirectX Math Support APIs]","XMBYTE4 constructor","XMBYTE4.XMBYTE4","XMBYTE4.XMBYTE4()","XMBYTE4.XMBYTE4(const float)","XMBYTE4::XMBYTE4","XMBYTE4::XMBYTE4(const float)","dxmath.xmbyte4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 9c8de507-9305-4b64-9176-46e662b22fae
ms.date: 05/06/2019
ms.keywords: XMBYTE4, XMBYTE4 constructor [DirectX Math Support APIs], XMBYTE4 constructor [DirectX Math Support APIs],XMBYTE4 structure, XMBYTE4 structure [DirectX Math Support APIs],XMBYTE4 constructor, XMBYTE4.XMBYTE4, XMBYTE4.XMBYTE4(), XMBYTE4.XMBYTE4(const float), XMBYTE4::XMBYTE4, XMBYTE4::XMBYTE4(const float), dxmath.xmbyte4_ctor_1
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
 - XMBYTE4::XMBYTE4
 - directxpackedvector/XMBYTE4::XMBYTE4
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
 - XMBYTE4.XMBYTE4
---

# XMBYTE4::XMBYTE4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a> from a four element <code>float</code> array argument.

This constructor initializes a new instance of <code>XMBYTE4</code> from a four element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>float</code> array containing the values used to initialize the four components of a new instance of **XMBYTE4**.

## -remarks

The magnitude of each member of the **pArray** argument to the constructor will be clamped to the range supported by an 8-bit signed integer [-127.0, 127.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMBYTE4 instance;

instance.x = (int8_t)min( max( pArray[0] -127.0 ), 127.0 );
instance.y = (int8_t)min( max( pArray[1] -127.0 ), 127.0 );
instance.z = (int8_t)min( max( pArray[2] -127.0 ), 127.0 );
instance.w = (int8_t)min( max( pArray[3] -127.0 ), 127.0 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a>

<a href="/windows/desktop/dxmath/xmbyte4-ctor">XMBYTE4 Constructors</a>