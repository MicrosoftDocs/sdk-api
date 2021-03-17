---
UID: NF:directxpackedvector.XMUBYTE2.XMUBYTE2(constfloat)
title: XMUBYTE2::XMUBYTE2(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTE2 from a two-element float array argument.
helpviewer_keywords: ["XMUBYTE2","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 structure","XMUBYTE2 structure [DirectX Math Support APIs]","XMUBYTE2 constructor","XMUBYTE2.XMUBYTE2","XMUBYTE2.XMUBYTE2()","XMUBYTE2.XMUBYTE2(const float)","XMUBYTE2::XMUBYTE2","XMUBYTE2::XMUBYTE2(const float)","dxmath.xmubyte2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 2b5e04aa-5847-499d-b67a-1f9fb1f4a596
ms.date: 05/06/2019
ms.keywords: XMUBYTE2, XMUBYTE2 constructor [DirectX Math Support APIs], XMUBYTE2 constructor [DirectX Math Support APIs],XMUBYTE2 structure, XMUBYTE2 structure [DirectX Math Support APIs],XMUBYTE2 constructor, XMUBYTE2.XMUBYTE2, XMUBYTE2.XMUBYTE2(), XMUBYTE2.XMUBYTE2(const float), XMUBYTE2::XMUBYTE2, XMUBYTE2::XMUBYTE2(const float), dxmath.xmubyte2_ctor_1
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
 - XMUBYTE2::XMUBYTE2
 - directxpackedvector/XMUBYTE2::XMUBYTE2
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
 - XMUBYTE2.XMUBYTE2
---

# XMUBYTE2::XMUBYTE2(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">XMUBYTE2</a> from a two-element <code>float</code> array argument.

This constructor initializes a new instance of **XMUBYTE2** from a two-element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available with C++.</div>

## -parameters

### -param pArray

Two-element **float** array containing the values used to initialize the two components of a new instance of **XMUBYTE2**.

## -remarks

The magnitude of each member of the *pArray* argument to the constructor will be clamped to the range supported by an 8-bit signed integer [0.0, 255.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTE2 instance;

instance.x = (uint8_t)min( max( pArray[0] 0.0 ), 255.0 );
instance.y = (uint8_t)min( max( pArray[1] 0.0 ), 255.0 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">XMUBYTE2</a>

<a href="/windows/desktop/dxmath/xmubyte2-ctor">XMUBYTE2 Constructors</a>