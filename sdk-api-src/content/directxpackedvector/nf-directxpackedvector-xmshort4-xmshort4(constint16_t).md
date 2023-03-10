---
UID: NF:directxpackedvector.XMSHORT4.XMSHORT4(constint16_t)
title: XMSHORT4::XMSHORT4(const int16_t) (directxpackedvector.h)
description: Initializes a new instance of XMSHORT4 from a four element int16_t array argument.
helpviewer_keywords: ["XMSHORT4","XMSHORT4 constructor [DirectX Math Support APIs]","XMSHORT4 constructor [DirectX Math Support APIs]","XMSHORT4 structure","XMSHORT4 structure [DirectX Math Support APIs]","XMSHORT4 constructor","XMSHORT4.XMSHORT4","XMSHORT4.XMSHORT4()","XMSHORT4.XMSHORT4(const int16_t)","XMSHORT4::XMSHORT4","XMSHORT4::XMSHORT4(const int16_t)","dxmath.xmshort4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 82a74ded-97db-4652-bd51-cf2660f4eaf0
ms.date: 05/06/2019
ms.keywords: XMSHORT4, XMSHORT4 constructor [DirectX Math Support APIs], XMSHORT4 constructor [DirectX Math Support APIs],XMSHORT4 structure, XMSHORT4 structure [DirectX Math Support APIs],XMSHORT4 constructor, XMSHORT4.XMSHORT4, XMSHORT4.XMSHORT4(), XMSHORT4.XMSHORT4(const int16_t), XMSHORT4::XMSHORT4, XMSHORT4::XMSHORT4(const int16_t), dxmath.xmshort4_ctor_1
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

# XMSHORT4::XMSHORT4(const int16_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a> from a four element <code>int16_t</code> array argument.

This constructor initializes a new instance of **XMSHORT4** from a from element <code>int16_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>int16_t</code> array containing the values used to initialize the four components of a new instance of **XMSHORT4**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMSHORT4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort4">XMSHORT4</a>

<a href="/windows/desktop/dxmath/xmshort4-ctor">XMSHORT4 Constructors</a>