---
UID: NF:directxpackedvector.XMSHORT2.XMSHORT2(constfloat)
title: XMSHORT2::XMSHORT2(const float) (directxpackedvector.h)
description: Initializes a new instance of XMSHORT2 from a two element float array argument.
helpviewer_keywords: ["XMSHORT2","XMSHORT2 constructor [DirectX Math Support APIs]","XMSHORT2 constructor [DirectX Math Support APIs]","XMSHORT2 structure","XMSHORT2 structure [DirectX Math Support APIs]","XMSHORT2 constructor","XMSHORT2.XMSHORT2","XMSHORT2.XMSHORT2()","XMSHORT2.XMSHORT2(const float)","XMSHORT2::XMSHORT2","XMSHORT2::XMSHORT2(const float)","dxmath.xmshort2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: d2ea9e07-f11f-4418-ac79-578f86eb8568
ms.date: 05/06/2019
ms.keywords: XMSHORT2, XMSHORT2 constructor [DirectX Math Support APIs], XMSHORT2 constructor [DirectX Math Support APIs],XMSHORT2 structure, XMSHORT2 structure [DirectX Math Support APIs],XMSHORT2 constructor, XMSHORT2.XMSHORT2, XMSHORT2.XMSHORT2(), XMSHORT2.XMSHORT2(const float), XMSHORT2::XMSHORT2, XMSHORT2::XMSHORT2(const float), dxmath.xmshort2_ctor_1
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
 - XMSHORT2::XMSHORT2
 - directxpackedvector/XMSHORT2::XMSHORT2
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
 - XMSHORT2.XMSHORT2
---

# XMSHORT2::XMSHORT2(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a> from a two element <code>float</code> array argument.

This constructor initializes a new instance of **XMSHORT2** from a two element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element <code>float</code> array containing the values used to initialize the two components of a new instance of **XMSHORT2**.

## -remarks

The magnitude of each member of the *pArray* argument to the constructor will be clamped to the range supported by a 16-bit signed integer [-32767.0, 32767.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMSHORT2 instance;

instance.x = (int16_t)min( max( pArray[0] -32767.0 ), 32767.0 );
instance.y = (int16_t)min( max( pArray[1] -32767.0 ), 32767.0 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a>

<a href="/windows/desktop/dxmath/xmshort2-ctor">XMSHORT2 Constructors</a>