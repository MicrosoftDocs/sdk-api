---
UID: NF:directxpackedvector.XMUSHORT4.XMUSHORT4(constuint16_t)
title: XMUSHORT4::XMUSHORT4(const uint16_t) (directxpackedvector.h)
description: Initializes a new instance of XMUSHORT4 from a four element uint16_t array argument.
helpviewer_keywords: ["XMUSHORT4","XMUSHORT4 constructor [DirectX Math Support APIs]","XMUSHORT4 constructor [DirectX Math Support APIs]","XMUSHORT4 structure","XMUSHORT4 structure [DirectX Math Support APIs]","XMUSHORT4 constructor","XMUSHORT4.XMUSHORT4","XMUSHORT4.XMUSHORT4()","XMUSHORT4.XMUSHORT4(const uint16_t)","XMUSHORT4::XMUSHORT4","XMUSHORT4::XMUSHORT4(const uint16_t)","dxmath.xmushort4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: c0ab2217-bca4-40b6-b875-a5b5c02f30d0
ms.date: 05/06/2019
ms.keywords: XMUSHORT4, XMUSHORT4 constructor [DirectX Math Support APIs], XMUSHORT4 constructor [DirectX Math Support APIs],XMUSHORT4 structure, XMUSHORT4 structure [DirectX Math Support APIs],XMUSHORT4 constructor, XMUSHORT4.XMUSHORT4, XMUSHORT4.XMUSHORT4(), XMUSHORT4.XMUSHORT4(const uint16_t), XMUSHORT4::XMUSHORT4, XMUSHORT4::XMUSHORT4(const uint16_t), dxmath.xmushort4_ctor_1
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

# XMUSHORT4::XMUSHORT4(const uint16_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort4">XMUSHORT4</a> from a four element <code>uint16_t</code> array argument.

This constructor initializes a new instance of **XMUSHORT4** from a four element <code>uint16_t</code> array argument.  

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element **uint16_t** array containing the values used to initialize the four components of a new instance of **XMUSHORT4**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUSHORT4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushort4">XMUSHORT4</a>

<a href="/windows/desktop/dxmath/xmushort4-ctor">XMUSHORT4 Constructors</a>