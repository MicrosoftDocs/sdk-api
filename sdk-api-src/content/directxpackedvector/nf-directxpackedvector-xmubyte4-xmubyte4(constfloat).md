---
UID: NF:directxpackedvector.XMUBYTE4.XMUBYTE4(constfloat)
title: XMUBYTE4::XMUBYTE4(const float) (directxpackedvector.h)
description: Initializes a new instance of XMUBYTE4 from a four element int8_t array argument.
helpviewer_keywords: ["XMUBYTE4","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 constructor [DirectX Math Support APIs]","XMUBYTE4 structure","XMUBYTE4 structure [DirectX Math Support APIs]","XMUBYTE4 constructor","XMUBYTE4.XMUBYTE4","XMUBYTE4.XMUBYTE4()","XMUBYTE4.XMUBYTE4(const float)","XMUBYTE4::XMUBYTE4","XMUBYTE4::XMUBYTE4(const float)","dxmath.xmubyte4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 89bc02ca-187d-4ffc-aac9-f3c0c57b23d5
ms.date: 05/06/2019
ms.keywords: XMUBYTE4, XMUBYTE4 constructor [DirectX Math Support APIs], XMUBYTE4 constructor [DirectX Math Support APIs],XMUBYTE4 structure, XMUBYTE4 structure [DirectX Math Support APIs],XMUBYTE4 constructor, XMUBYTE4.XMUBYTE4, XMUBYTE4.XMUBYTE4(), XMUBYTE4.XMUBYTE4(const float), XMUBYTE4::XMUBYTE4, XMUBYTE4::XMUBYTE4(const float), dxmath.xmubyte4_ctor_1
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

# XMUBYTE4::XMUBYTE4(const float)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a> from a four element <code>int8_t</code> array argument.

This constructor initializes a new instance of **XMUBYTE4** from a four element <code>int8_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element *int8_t* array containing the values used to initialize the four components of a new instance of **XMUBYTE4** .

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTE4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte4">XMUBYTE4</a>

<a href="/windows/desktop/dxmath/xmubyte4-ctor">XMUBYTE4 Constructors</a>