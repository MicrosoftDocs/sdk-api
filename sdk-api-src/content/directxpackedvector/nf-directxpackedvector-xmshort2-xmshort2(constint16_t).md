---
UID: NF:directxpackedvector.XMSHORT2.XMSHORT2(constint16_t)
title: XMSHORT2::XMSHORT2(const int16_t) (directxpackedvector.h)
description: Initializes a new instance of XMSHORT2 from a two element int16_t array argument.
helpviewer_keywords: ["XMSHORT2","XMSHORT2 constructor [DirectX Math Support APIs]","XMSHORT2 constructor [DirectX Math Support APIs]","XMSHORT2 structure","XMSHORT2 structure [DirectX Math Support APIs]","XMSHORT2 constructor","XMSHORT2.XMSHORT2","XMSHORT2.XMSHORT2()","XMSHORT2.XMSHORT2(const int16_t)","XMSHORT2::XMSHORT2","XMSHORT2::XMSHORT2(const int16_t)","dxmath.xmshort2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: e36f1ccb-521a-41ce-87da-e1dd995f742c
ms.date: 05/06/2019
ms.keywords: XMSHORT2, XMSHORT2 constructor [DirectX Math Support APIs], XMSHORT2 constructor [DirectX Math Support APIs],XMSHORT2 structure, XMSHORT2 structure [DirectX Math Support APIs],XMSHORT2 constructor, XMSHORT2.XMSHORT2, XMSHORT2.XMSHORT2(), XMSHORT2.XMSHORT2(const int16_t), XMSHORT2::XMSHORT2, XMSHORT2::XMSHORT2(const int16_t), dxmath.xmshort2_ctor_1
f1_keywords:
- directxpackedvector/XMSHORT2.XMSHORT2
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
req.namespace: DirectX::PackedVector
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
- DirectXPackedVector.h
api_name:
- XMSHORT2.XMSHORT2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMSHORT2::XMSHORT2(const int16_t)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a> from a two element <code>int16_t</code> array argument.

This constructor initializes a new instance of **XMSHORT2** from a two element <code>int16_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Two element <code>int16_t</code> array containing the values used to initialize the two components of a new instance of **XMSHORT2**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMSHORT2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmshort2">XMSHORT2</a>

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmshort2-ctor">XMSHORT2 Constructors</a>
