---
UID: NF:directxpackedvector.XMUBYTEN4.XMUBYTEN4(constuint8_t)
title: XMUBYTEN4::XMUBYTEN4(const uint8_t) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTEN4 from a four element uint8_t array argument.
helpviewer_keywords: ["XMUBYTEN4","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 constructor [DirectX Math Support APIs]","XMUBYTEN4 structure","XMUBYTEN4 structure [DirectX Math Support APIs]","XMUBYTEN4 constructor","XMUBYTEN4.XMUBYTEN4","XMUBYTEN4.XMUBYTEN4()","XMUBYTEN4.XMUBYTEN4(const uint8_t)","XMUBYTEN4::XMUBYTEN4","XMUBYTEN4::XMUBYTEN4(const uint8_t)","dxmath.xmubyten4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 7e5d6c9b-3371-456d-8d4c-1663934b43be
ms.date: 05/06/2019
ms.keywords: XMUBYTEN4, XMUBYTEN4 constructor [DirectX Math Support APIs], XMUBYTEN4 constructor [DirectX Math Support APIs],XMUBYTEN4 structure, XMUBYTEN4 structure [DirectX Math Support APIs],XMUBYTEN4 constructor, XMUBYTEN4.XMUBYTEN4, XMUBYTEN4.XMUBYTEN4(), XMUBYTEN4.XMUBYTEN4(const uint8_t), XMUBYTEN4::XMUBYTEN4, XMUBYTEN4::XMUBYTEN4(const uint8_t), dxmath.xmubyten4_ctor_1
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
 - XMUBYTEN4::XMUBYTEN4
 - directxpackedvector/XMUBYTEN4::XMUBYTEN4
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
 - XMUBYTEN4.XMUBYTEN4
---

# XMUBYTEN4::XMUBYTEN4(const uint8_t)


## -description

Initializes a new instance of <a href="/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a> from a four element <code>uint8_t</code> array argument.

This constructor initializes a new instance of **XMUBYTEN4** from a four element <code>uint8_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element *uint8_t* array containing the values used to initialize the four components of a new instance of **XMUBYTEN4**.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTEN4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];

```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyten4">XMUBYTEN4</a>

<a href="/windows/desktop/dxmath/xmubyten4-ctor">XMUBYTEN4 Constructors</a>
