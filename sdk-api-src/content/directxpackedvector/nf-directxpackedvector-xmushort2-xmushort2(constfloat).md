---
UID: NF:directxpackedvector.XMUSHORT2.XMUSHORT2(const float)
title: XMUSHORT2::XMUSHORT2(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUSHORT2 from a two element float array argument.
old-location: 
tech.root: dxmath
ms.assetid: 226e51fe-eddc-430a-ba9d-faf7496c5c86
ms.date: 05/06/2019
ms.keywords: XMUSHORT2, XMUSHORT2 constructor [DirectX Math Support APIs], XMUSHORT2 constructor [DirectX Math Support APIs],XMUSHORT2 structure, XMUSHORT2 structure [DirectX Math Support APIs],XMUSHORT2 constructor, XMUSHORT2.XMUSHORT2, XMUSHORT2.XMUSHORT2(), XMUSHORT2.XMUSHORT2(const float), XMUSHORT2::XMUSHORT2, XMUSHORT2::XMUSHORT2(const float), dxmath.xmushort2_ctor_1
ms.topic: method
f1_keywords:
- directxpackedvector/XMUSHORT2.XMUSHORT2
dev_langs:
- c++
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
req.namespace: Use DirectX.
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- directxpackedvector.h
api_name:
- XMUSHORT2.XMUSHORT2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUSHORT2::XMUSHORT2(const float)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort2">XMUSHORT2</a> from a two element <code>float</code> array argument.

This constructor initializes a new instance of **XMUSHORT2** from a from a two element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element **float** array containing the values used to initialize the two components of a new instance of XMUSHORT2.

## -remarks

The magnitude of each member of the *pArray* argument to the constructor will be clamped to the range supported by an 16-bit unsigned integer [0.0, 65535.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUSHORT2 instance;

instance.x = (uint16_t)min( max( pArray[0] 0.0 ), 65535.0 );
instance.y = (uint16_t)min( max( pArray[1] 0.y0 ), 65535.0 );
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort2">XMUSHORT2</a>

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmushort2-ctor">XMUSHORT2 Constructors</a>
