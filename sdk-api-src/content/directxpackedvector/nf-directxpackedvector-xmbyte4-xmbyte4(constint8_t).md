---
UID: NF:directxpackedvector.XMBYTE4.XMBYTE4(constint8_t)
title: XMBYTE4::XMBYTE4(const int8_t) (directxpackedvector.h)
description: Initializes a new instance of XMBYTE4 from a four element int8_t array argument.
helpviewer_keywords: ["XMBYTE4","XMBYTE4 constructor [DirectX Math Support APIs]","XMBYTE4 constructor [DirectX Math Support APIs]","XMBYTE4 structure","XMBYTE4 structure [DirectX Math Support APIs]","XMBYTE4 constructor","XMBYTE4.XMBYTE4","XMBYTE4.XMBYTE4()","XMBYTE4.XMBYTE4(const int8_t)","XMBYTE4::XMBYTE4","XMBYTE4::XMBYTE4(const int8_t)","dxmath.xmbyte4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 5525efe0-7377-40ae-a52d-5a54dbdfa0cd
ms.date: 05/06/2019
ms.keywords: XMBYTE4, XMBYTE4 constructor [DirectX Math Support APIs], XMBYTE4 constructor [DirectX Math Support APIs],XMBYTE4 structure, XMBYTE4 structure [DirectX Math Support APIs],XMBYTE4 constructor, XMBYTE4.XMBYTE4, XMBYTE4.XMBYTE4(), XMBYTE4.XMBYTE4(const int8_t), XMBYTE4::XMBYTE4, XMBYTE4::XMBYTE4(const int8_t), dxmath.xmbyte4_ctor_1
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

# XMBYTE4::XMBYTE4(const int8_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a> from a four element <code>int8_t</code> array argument.

This constructor initializes a new instance of **XMBYTE4** from a from a four element <code>int8_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element <code>int8_t</code> array containing the values used to initialize the four components of a new instance of **XMBYTE4**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMBYTE4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmbyte4">XMBYTE4</a>

<a href="/windows/desktop/dxmath/xmbyte4-ctor">XMBYTE4 Constructors</a>