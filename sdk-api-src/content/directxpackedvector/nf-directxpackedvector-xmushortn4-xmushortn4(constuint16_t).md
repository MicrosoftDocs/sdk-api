---
UID: NF:directxpackedvector.XMUSHORTN4.XMUSHORTN4(constuint16_t)
title: XMUSHORTN4::XMUSHORTN4(const uint16_t) (directxpackedvector.h)
description: Initializes a new instance of XMUSHORTN4 from a four element uint16_t array argument.
helpviewer_keywords: ["XMUSHORTN4","XMUSHORTN4 constructor [DirectX Math Support APIs]","XMUSHORTN4 constructor [DirectX Math Support APIs]","XMUSHORTN4 structure","XMUSHORTN4 structure [DirectX Math Support APIs]","XMUSHORTN4 constructor","XMUSHORTN4.XMUSHORTN4","XMUSHORTN4.XMUSHORTN4()","XMUSHORTN4.XMUSHORTN4(const uint16_t)","XMUSHORTN4::XMUSHORTN4","XMUSHORTN4::XMUSHORTN4(const uint16_t)","dxmath.xmushortn4_ctor_1"]
old-location: 
tech.root: dxmath
ms.assetid: 2fd23876-f0d0-4be5-b22a-38d8cbbc60ec
ms.date: 05/06/2019
ms.keywords: XMUSHORTN4, XMUSHORTN4 constructor [DirectX Math Support APIs], XMUSHORTN4 constructor [DirectX Math Support APIs],XMUSHORTN4 structure, XMUSHORTN4 structure [DirectX Math Support APIs],XMUSHORTN4 constructor, XMUSHORTN4.XMUSHORTN4, XMUSHORTN4.XMUSHORTN4(), XMUSHORTN4.XMUSHORTN4(const uint16_t), XMUSHORTN4::XMUSHORTN4, XMUSHORTN4::XMUSHORTN4(const uint16_t), dxmath.xmushortn4_ctor_1
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
 - XMUSHORTN4::XMUSHORTN4
 - directxpackedvector/XMUSHORTN4::XMUSHORTN4
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
 - XMUSHORTN4.XMUSHORTN4
---

# XMUSHORTN4::XMUSHORTN4(const uint16_t)


## -description

Initializes a new instance of <a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn4">XMUSHORTN4</a> from a four element <code>uint16_t</code> array argument.

This constructor initializes a new instance of **XMUSHORTN4** from a four element <code>uint16_t</code> array argument.

<div class="alert"><b>Note</b>  This constructor is only available under C++.</div>

## -parameters

### -param pArray

Four element **uint16_t** array containing the values used to initialize the four components of a new instance of **XMUSHORTN4**.

## -remarks

Input values are not normalized. The following pseudocode demonstrates the operation of this constructor:

```cpp
XMUSHORTN4 instance;
instance.x = pArray[0];
instance.y = pArray[1];
instance.z = pArray[2];
instance.w = pArray[3];
```

## -see-also

<a href="/windows/desktop/api/directxpackedvector/ns-directxpackedvector-xmushortn4">XMUSHORTN4</a>

<a href="/windows/desktop/dxmath/xmushortn4-ctor">XMUSHORTN4 Constructors</a>