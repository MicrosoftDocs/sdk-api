---
UID: NF:directxpackedvector.XMUBYTE2.XMUBYTE2(constuint8_t)
title: XMUBYTE2::XMUBYTE2(const uint8_t) (directxpackedvector.h)
description: Initializes a new instance of **XMUBYTE2** from a two-element int8_t array argument.
helpviewer_keywords: ["XMUBYTE2","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 constructor [DirectX Math Support APIs]","XMUBYTE2 structure","XMUBYTE2 structure [DirectX Math Support APIs]","XMUBYTE2 constructor","XMUBYTE2.XMUBYTE2","XMUBYTE2.XMUBYTE2()","XMUBYTE2.XMUBYTE2(const uint8_t)","XMUBYTE2::XMUBYTE2","XMUBYTE2::XMUBYTE2(const uint8_t)","dxmath.xmubyte2_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: d7f51876-9fc9-40b7-8b42-ff4ee4c9afa0
ms.date: 05/06/2019
ms.keywords: XMUBYTE2, XMUBYTE2 constructor [DirectX Math Support APIs], XMUBYTE2 constructor [DirectX Math Support APIs],XMUBYTE2 structure, XMUBYTE2 structure [DirectX Math Support APIs],XMUBYTE2 constructor, XMUBYTE2.XMUBYTE2, XMUBYTE2.XMUBYTE2(), XMUBYTE2.XMUBYTE2(const uint8_t), XMUBYTE2::XMUBYTE2, XMUBYTE2::XMUBYTE2(const uint8_t), dxmath.xmubyte2_ctor_1
f1_keywords:
- directxpackedvector/XMUBYTE2.XMUBYTE2
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
- XMUBYTE2.XMUBYTE2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# XMUBYTE2::XMUBYTE2(const uint8_t)

## -description

Initializes a new instance of <a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">**XMUBYTE2**</a> from a two-element <code>int8_t</code> array argument.

This constructor initializes a new instance of **XMUBYTE2** from a two-element <code>int8_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available with C++.</div>

## -parameters

### -param pArray

Two-element **int8_t** array containing the values used to initialize the two components of a new instance of **XMUBYTE2**.

## -remarks

The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUBYTE2 instance;
instance.x = pArray[0];
instance.y = pArray[1];
```

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmubyte2">XMUBYTE2</a>

<a href="https://docs.microsoft.com/windows/desktop/dxmath/xmubyte2-ctor">XMUBYTE2 Constructors</a>
