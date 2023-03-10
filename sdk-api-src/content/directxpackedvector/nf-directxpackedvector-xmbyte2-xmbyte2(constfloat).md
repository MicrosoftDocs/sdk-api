---
UID: NF:directxpackedvector.XMBYTE2.XMBYTE2(constfloat)
title: XMBYTE2::XMBYTE2(const float) (directxpackedvector.h)
description: Initializes a new instance of XMBYTE2 from a two-element float array argument.
helpviewer_keywords: ["XMBYTE2","XMBYTE2 constructor [DirectX Math Support APIs]","XMBYTE2 constructor [DirectX Math Support APIs]","XMBYTE2 structure","XMBYTE2 structure [DirectX Math Support APIs]","XMBYTE2 constructor","XMBYTE2.XMBYTE2","XMBYTE2.XMBYTE2()","XMBYTE2.XMBYTE2(const float)","XMBYTE2::XMBYTE2","XMBYTE2::XMBYTE2(const float)","dxmath.xmbyte2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 958e88f3-97cb-4a26-abcf-cbb8185f4716
ms.date: 05/06/2019
ms.keywords: XMBYTE2, XMBYTE2 constructor [DirectX Math Support APIs], XMBYTE2 constructor [DirectX Math Support APIs],XMBYTE2 structure, XMBYTE2 structure [DirectX Math Support APIs],XMBYTE2 constructor, XMBYTE2.XMBYTE2, XMBYTE2.XMBYTE2(), XMBYTE2.XMBYTE2(const float), XMBYTE2::XMBYTE2, XMBYTE2::XMBYTE2(const float), dxmath.xmbyte2_ctor_1
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
 - XMBYTE2::XMBYTE2
 - directxpackedvector/XMBYTE2::XMBYTE2
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
 - XMBYTE2.XMBYTE2
---

# XMBYTE2::XMBYTE2(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte2">XMBYTE2</a> from a two-element <code>float</code> array argument.

This constructor initializes a new instance of **XMBYTE2** from a two-element <code>float</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available with C++.</div>

## -parameters

### -param pArray

Two-element <code>float</code> array containing the values used to initialize the two components of a new instance of **XMBYTE2**.

## -remarks

The magnitude of each member of the **pArray** argument to the constructor will be clamped to the range supported by an 8-bit signed integer [-127.0, 127.0].

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMBYTE2 instance;

instance.x = (int8_t)min( max( pArray[0] -127.0 ), 127.0 );
instance.y = (int8_t)min( max( pArray[1] -127.0 ), 127.0 );
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte2">XMBYTE2</a>

<a href="/windows/desktop/dxmath/xmbyte2-ctor">XMBYTE2 Constructors</a>